<template>
    <header>
        <div class="header">
            <div class="inner">
                <div id="logo-wrap">
                    <a href="#"><img src="@/assets/svg/logo.png"></a>
                </div>
                <nav id="main-nav">
                    <router-link v-for="(item, index) in navItems" :key="index" :to="item.url" class="main-nav-link">{{item.name}}</router-link>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    navItems: {
      type: Array,
      required: true,
      default: () => []
    }
  }
}
</script>
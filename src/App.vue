<template>
 <NavComponents/>
  <router-view />
  <FooterComponent/>
</template>

<style lang="scss">
body{
  font-family: 'Sora';
  font-weight: 200;
  overflow-x: hidden;
}
#app {
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
<script>
import NavComponents from "@/views/components/nav-components";
import FooterComponent from "@/views/components/footer-component";
export default {
  components: { FooterComponent, NavComponents }
}
</script>
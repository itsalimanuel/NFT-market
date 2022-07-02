<template>
 <NavComponents/>
  <router-view />
</template>

<style lang="scss">
body{
  font-family: 'Sora';
  font-weight: 200;
  overflow-x: hidden;
}
#app {
  text-align: center;
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
export default {
  components: { NavComponents }
}
</script>
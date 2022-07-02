<template>
  <div class="list">
    <el-link :underline="false" href="" target="_blank">
      <img :src="require('@/assets/imgs/brands/ritter-sport.svg')" alt="sport">
    </el-link>
    <el-link :underline="false" href="" target="_blank">
      <img :src="require('@/assets/imgs/brands/nike.svg')" alt="nike">
    </el-link>
    <el-link :underline="false" href="" target="_blank">
      <img :src="require('@/assets/imgs/brands/adidas.svg')" alt="adidas">
    </el-link>
    <el-link :underline="false" href="" target="_blank">
      <img :src="require('@/assets/imgs/brands/holland.svg')" alt="">
    </el-link>
  </div>
</template>

<script>
export default {
  name: "index"
};
</script>

<style scoped lang="sass">
.list
  position: relative
  margin-top: auto
  max-width: 643px
  display: grid
  width: 100%
  grid-template-columns: repeat(4, 1fr)

  a
    width: 85px
    height: 25px
    margin: auto

    span
      width: 100%
      height: 100%

    img
      width: 100%
      height: 100%

    &:hover
      text-decoration: none

</style>
<style lang="scss">
.list {
  a {
    &:hover {
      text-decoration: none;
    }
  }

  a span {
    width: 100%;
    height: 100%
  }
}
</style>
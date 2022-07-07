<template>
  <div class="auctions">
    <div class="auctions-title">
      <h2>Latest live auctions</h2>
    </div>
    <div class="auctions-slider">
      <Slider />
    </div>
    <div class="auctions-more">
      <el-link :underline="false" href="/auctions">
        <span>more</span>
        <svg width="13px" height="10px" viewBox="0 0 13 10">
          <path d="M1,5 L11,5"></path>
          <polyline points="8 1 12 5 8 9"></polyline>
        </svg>
      </el-link>
    </div>
  </div>
</template>

<script>
import Slider from "@/views/blocs/auctions-bloc/slider";

export default {
  name: "index",
  components: { Slider },
};
</script>

<style lang="sass" scoped>
.auctions
  position: relative
  margin-top: 65px
  margin-bottom: 65px

  &-title

  text-align: center

  h2
    color: #060714
    font-weight: 600
    font-size: 26px
    line-height: 45px
    letter-spacing: 0.2px
    margin-bottom: 50px
  &-more a
    text-transform: uppercase
    display: flex
    max-width: 90px
    margin: auto
    padding:
      top: 10px
      bottom: 10px
      right: 10px
      left: 10px
    position: relative
    transition: all 0.5s ease
    span
      font-size: 14px
      letter-spacing: 1.5px
      line-height: 100%
      color: #060714
    &:before
      content: ""
      position: absolute
      transition: all 0.5s ease
      top: 0
      left: 0
      display: block
      border-radius: 28px
      background: rgba(49,49,191,.5)
      width: 35px
      height: 35px
    &:hover
      text-decoration: none
      &:before
        width: 100%

    svg
      position: relative
      top: 0
      margin-left: 10px
      fill: none
      stroke-linecap: round
      stroke-linejoin: round
      stroke: #000
      stroke-width: 2
      transform: translateX(-5px)
      transition: all .3s ease
    &:hover
      &:before
        width: 100%
        background-color: rgba(49,49,191,.5)
        transition: all .3s ease
      svg
        transform: translateX(0)


</style>


<style lang="sass">
a
  text-decoration: none
  &:hover
    text-decoration: none

</style>
<template>
  <div class="get-start">
    <div class="get-start-box">
      <div class="get-start-image">
        <img :src="require('@/assets/imgs/hand.svg')" alt="hand" />
      </div>
      <div class="get-start-content">
        <div class="get-start-title">
          <h3>Get started creating & selling your NFTs</h3>
        </div>
        <div class="get-start-description">
          <p>
            Nunc gravida faucibus netus feugiat tellus, viverra massa feugiat.
            Mi est sit.
          </p>
        </div>
        <div class="get-start-link">
          <el-link href="" :underline="false"> Get started </el-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "get-start",
};
</script>

<style scoped lang="sass">

.get-start
  background-color: #000
  position: relative
  //border-radius: 20px
  border-radius: 0 20px 20px 20px

  &:before
    position: absolute
    top: 0
    content: ''
    left: 0
    background-position: center
    background-size: cover
    background-image: url('../../../assets/icons/pleat.svg')
    transform: translateY(-100%)
    height: 20px
    width: 180px

  &-box
    padding:
      top: 0
      left: 0
      right: 0
      bottom: 40px

  &-image
    width: 100%

    img
      border-top-right-radius: 20px
      border-top-left-radius: 20px
      width: 100%
      height: 100%

  &-content
    text-align: left
    display: flex
    flex-direction: column
    padding:
      top: 12px
      left: 40px
      right: 40px
      bottom: 40px

  &-title
    padding-right: 60px
    h3
      color: #FFFFFF
      letter-spacing: 0.2px
      line-height: 125%
      font-size: 24px
      font-weight: 600
  &-description
    margin-top: 15px
    p
      color: #7780A1
      letter-spacing: 0.2px
      font-size: 14px
      font-weight: 400

  &-link
    margin-top: 50px
    text-align: center
    border-radius: 12px
    background: linear-gradient(104.42deg, #4745D0 0%, #2A27C9 60.23%)
    a
      padding: 16px
      color: #FFFFFF
      letter-spacing: 0.2px
      text-align: center

</style>

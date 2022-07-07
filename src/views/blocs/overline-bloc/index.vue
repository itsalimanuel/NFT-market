<template>
  <div class="overline">
    <div class="overline-content">
      <div class="overline-sub">
        <h3>Overline</h3>
      </div>
      <div class="overline-title">
        <h2>Sapien ipsum scelerisque convallis fusce</h2>
      </div>
      <div class="overline-description">
        <p>
          Ut amet vulputate faucibus vitae semper eget auctor. Diam tempor
          pulvinar ultricies dolor feugiat aliquam commodo.
        </p>
      </div>
      <div class="overline-links">
        <el-link :underline="false" class="get"> Get Started </el-link>
        <el-link :underline="false" class="learn"> Learn more </el-link>
      </div>
    </div>
    <div class="overline-image">
      <el-image lazy :src="require('@/assets/imgs/getStarted.svg')" alt="image"></el-image>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
};
</script>

<style lang="sass" scoped>
.overline
  max-width: 1250px
  width: 100%
  margin: auto
  display: grid
  grid-template-columns: repeat(2,1fr)
  align-items: center

  &-image
    max-height: 616px
    img
      height: 100%
      width: 100%
  &-content
    max-width: 590px
    padding-right: 100px
    text-align: left
  &-sub
    letter-spacing: 3px
    text-transform: uppercase
    h3
      color: #BBC0D0
      font-weight: 400
      font-size: 15px
      line-height: 18px
      margin-bottom: 16px
  &-title
    h2
      font-weight: 600
      font-size: 50px
      line-height: 100%
      color: #060714
      letter-spacing: 0.2px
      margin-bottom: 32px
  &-description
    color: #7780A1
    line-height: 150%
    font-weight: 400
    font-size: 14px
    padding-right: 100px
  &-links
    margin-top: 40px
    a
      padding: 12px 18px
      font-size: 14px
      letter-spacing: 0.2px
      line-height: 20px
      font-weight: 600
    .get
      background: linear-gradient(104.42deg, #4745D0 0%, #2A27C9 60.23%)
      color: #ffffff
      border-radius: 12px
    .learn
      margin-left: 10px
      border: 2px solid #7780A1
      border-radius: 12px
      color: #7780A1
      letter-spacing: 0.2px

</style>

<template>
  <div class="habitant">
    <div class="habitant-image">
      <img :src="require('@/assets/imgs/habitant-image.jpg')" alt="habitant" />
    </div>
    <div class="habitant-content">
      <div class="habitant-subtitle">
        <span>Overline</span>
      </div>
      <div class="habitant-title">
        <h2>Habitant tristique aliquam in vel scelerisque</h2>
      </div>
      <div class="habitant-description">
        <p>
          Ut amet vulputate faucibus vitae semper eget auctor. Diam tempor pulvinar ultricies dolor feugiat aliquam commodo.
        </p>
      </div>
      <div class="habitant-list">
        <div class="habitant-item">
          <div class="habitant-item-icon">
            <img :src="require('@/assets/icons/sollicitudin.svg')" alt="" />
          </div>
          <div class="habitant-item-title">
            <h4>Sollicitudin sapien</h4>
          </div>
          <div class="habitant-item-desc">
            <p>Cursus fermentum</p>
          </div>
        </div>
        <div class="habitant-item">
          <div class="habitant-item-icon">
            <img :src="require('@/assets/icons/Pulvinar.svg')" alt="" />
          </div>
          <div class="habitant-item-title">
            <h4>Sollicitudin sapien</h4>
          </div>
          <div class="habitant-item-desc">
            <p>Cursus fermentum</p>
          </div>
        </div>
      </div>
      <div class="habitant-links">
        <el-link :underline="false" class="get">Get start</el-link>
        <el-link :underline="false" class="learn">Learn more</el-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
};
</script>

<style scoped lang="sass">
.habitant
  display: grid
  grid-template-columns: repeat(2,1fr)
  grid-gap: 5px
  max-width: 1300px
  width: 100%
  margin:
    top: 0
    left: auto
    right: auto
    bottom: 0
  &-image
    width: 100%
    height: 100%
    img
      width: 100%
      height: 100%
  &-content
    text-align: left
  &-subtitle
      span
        color: #BBC0D0
        letter-spacing: 2px
        font-size: 15px
        font-weight: 500
        line-height: 18px
  &-title
      margin-top: 16px
      display: block
      h2
        color: #060714
        font-size: 64px
        letter-spacing: 0.2px
        font-weight: 600
        line-height: 100%
  &-description
    margin-top: 32px
    p
      color: #7780A1
      letter-spacing: 0.2px
      line-height: 150%
      font-weight: 300
      font-size: 16px
  &-list
    margin-top: 40px
    display: grid
    grid-gap: 24px
    max-width: 450px
    grid-template-columns: repeat(2,1fr)
  &-item
    position: relative
    &-icon
      width: 30px
      height: 30px
      margin-bottom: 24px
    &-title
      h4
        color: #060714
        letter-spacing: 0.2px
        line-height: 25px
        font-size: 20px
        font-weight: 600
    &-desc
      p
        color: #7780A1
        font-size: 14px
        line-height: 150%
        font-weight: 300
  &-links
      margin-top: 40px
      display: flex

</style>
<style lang="sass">
a.get
  background: linear-gradient(104.42deg, #4745D0 0%, #2A27C9 60.23%)
  border-radius: 12px
  font-size: 14px
  letter-spacing: 0.2px
  padding: 12px 22px
  color: #fff
  transition: 0.2s ease
  &:hover
    color: #fff
a.learn
  margin-left: 12px
  border-radius: 12px
  font-size: 14px
  letter-spacing: 0.2px
  padding: 12px 22px
  color: #7780A1
  border: 2px solid #7780A1
  transition: 0.2s ease
  &:hover
    color: #4745D0
</style>
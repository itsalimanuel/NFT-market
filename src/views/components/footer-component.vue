<template>
  <footer class="footer">
    <div class="footer-list">
      <div class="footer-brand">
        <div class="footer-logo">
          <img :src="require('@/assets/logo.svg')" alt="">
        </div>
        <div class="footer-pages">
          <el-link :underline="false" class="legal-page">Support</el-link>
          <el-link :underline="false" class="legal-page">Term of service</el-link>
          <el-link :underline="false" class="legal-page">License</el-link>
        </div>
      </div>
      <div class="footer-links">
        <div class="links">
          <el-link :underline="false" class="footer-link">Auctions</el-link>
          <el-link :underline="false" class="footer-link">Roadmap</el-link>
          <el-link :underline="false" class="footer-link">Discover</el-link>
          <el-link :underline="false" class="footer-link">Community</el-link>
        </div>
        <div class="action">
          <el-link :underline="false">My account</el-link>
        </div>
      </div>
      <div class="footer-info">
        <div class="footer-description">
          <p>
            Nibh volutpat, aliquam id sagittis elementum. Pellentesque laoreet velit, sed egestas in. Id nam semper
            dolor tellus vulputate eget turpis.
          </p>
        </div>
        <div class="footer-newsletter">
          <el-form-item class="form" label="">
            <el-input class="form-search" v-model="inputEmail" placeholder="Newsletter"></el-input>
            <el-button class="form-btn">Sign in</el-button>
          </el-form-item>
        </div>
      </div>
    </div>
  </footer>
  <template>
    <div class="copyright" v-show="dateTime"></div>
  </template>
</template>

<script>
export default {
  name: "footer-component",
  data() {
    return {
      inputEmail: "",
      dateTime:'2022'
    };
  },

};
</script>

<style lang="sass" scoped>
.footer
  width: 100%
  max-width: 1200px
  position: relative
  border: 1px solid #E2E2ED
  border-radius: 20px
  margin:
    top: 50px
    left: auto
    right: auto
    bottom: 50px

  &-list
    display: grid
    width: 100%
    grid-template-columns: repeat(3, 1fr)
    text-align: left

  &-brand
    padding: 40px
    height: 100%

  &-logo
    height: 30px
    width: 200px

    img
      width: 100%
      height: 100%

  &-pages
    margin-top: 150px
    display: flex
    align-items: center

  &-links
    position: relative
    padding: 40px
    text-align: left

    .links
      display: block

  &-info
    position: relative
    display: inline-grid
    padding: 40px

    p
      font-size: 14px

  &-newsletter
    margin-top: auto
    box-shadow: 0px 25px 75px rgba(6, 7, 20, 0.1)
    border-radius: 16px

    .form
      position: relative
      height: 45px
      width: 100%
      margin-bottom: 0

      &-search
        height: 100%
        width: 100%
        color: #7780A1

      &-btn

.copyright
  text-align: center
  margin-bottom: 10px


</style>

<style lang="sass">
.legal-page
  margin-right: 30px
  word-break: normal

  &:hover
    span
      color: #2c3e50

  span
    font-size: 12px
    color: #7780A1
    font-weight: 300
    letter-spacing: 0.2px
    line-height: 140%

.links
  text-align: left

  .footer-link
    display: block
    margin-bottom: 16px

.action
  margin-top: auto

  a
    display: inline-block
    border-radius: 12px
    background: linear-gradient(104.42deg, rgba(255, 255, 255, 0.15) 0%, rgba(255, 255, 255, 0) 60.23%), #2A27C9
    padding: 10px 18px

    span
      color: #fff
      line-height: 00%

.form button
  position: absolute
  top: 50%
  right: 16px
  transform: translateY(-50%)
  color: #2A27C9
  letter-spacing: 0.2px
  font-weight: 600
  font-size: 14px
</style>
<template>
  <el-form class="form">
    <el-input v-model="search" class="form-search" model-value="" placeholder="Search for item"
              type="search"></el-input>
    <select class="form-select" name="select" id="select">
      <option value="NFT">NFT</option>
      <option value="COIN">COIN</option>
      <option value="ELSE">ELSE</option>
    </select>
    <el-button class="form-btn">
      <img :src='require("@/assets/icons/search-blue.svg")' alt="search">
    </el-button>
  </el-form>
</template>

<script>
export default {
  name: "index.vue",
  data() {
    return {
      select: "",
      search: ""
    };
  }
};
</script>

<style scoped lang="sass">
.form
  margin-top: 20px
  position: relative
  max-width: 643px
  width: 100%
  height: 50px
  background-color: #ffffff
  box-shadow: 0px 25px 75px rgba(6, 7, 20, 0.1)
  border-radius: 16px
  display: flex
  align-items: center
  overflow: hidden

  &-search
    position: relative
    height: 100%
    font-size: 14px
    font-weight: 400
    letter-spacing: 0.2px
    color: #999
    opacity: 0.5
    background-color: transparent
    border: none
    padding: 20px 18px

    &:after
      position: absolute
      content: ''
      right: 0
      height: 50%
      width: 1px
      top: 50%
      transform: translateY(-50%)
      opacity: 0.25
      border: 0.5px solid #1F2A47

  &-select
    height: 100%
    border: 1px solid #fff
    font-size: 14px
    font-weight: 400
    color: #BBC0D0

    div
      height: 100%
      border: none

  &-btn
    height: 100%

    img
      width: 24px
      height: 24px
</style>

<style lang="scss">
.form {
  &-select {
    background-color: transparent;
    border: none;

    div {
      height: 100%;
      box-shadow: none !important;
    }
  }

  input {
    box-shadow: none;
    outline: none;
  }

  .el-input__wrapper {
    box-shadow: none !important;
    color: #BBC0D0;

    option {
      color: #BBC0D0;
    }
  }

  .el-select .el-input__inner {
    color: #BBC0D0;
  }

  button {
    box-shadow: none !important;
    border: none;

    &:hover {
      background-color: transparent;
    }
  }
}
</style>

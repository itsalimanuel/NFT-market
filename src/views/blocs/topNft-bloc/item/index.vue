<template>
  <div class="item">
    <div class="item-image">
      <img :src="require('@/assets/imgs/nft/item-2.jpg')" alt="" />
    </div>
    <div class="item-content">
      <div class="item-title">
        <h3>Vulputate velit viverra volutpat volutpat tristique</h3>
      </div>
      <div class="item-timer">
        <div class="time">
          <img :src="require('@/assets/icons/timer.svg')" alt="Timer">
          <span>20:00</span>
        </div>
        <div class="cost">1.3ETH</div>
      </div>
      <div class="item-follower">
        <div class="item-follower-number">101 people are bidding</div>
        <button>
          <img
            v-if="like"
            :src="require('@/assets/icons/heart-empty.svg')"
            alt=""
          />
          <img v-else :src="require('@/assets/icons/heart-red.svg')" alt="" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      like: false,
    };
  },
};
</script>

<style scoped lang="sass">
.item
  display: grid
  grid-template-columns: 1fr 2fr
  grid-gap: 10px
  &-image
    height: 120px
    width: 100%
    img
      border-radius: 20px
      width: 100%
      height: 100%
  &-content
    padding-right: 20px
    text-align: left
    position: relative
  &-title
    h3
      color: #060714
      line-height: 20px
      letter-spacing: 0.2px
      font-weight: 700
      font-size: 16px

  &-timer
    margin-top: 16px
    display: flex
    align-items: center
    justify-content: space-between
    .time
      display: flex
      align-items: center
      img
        width: 14.22px
        height: 16px
      span
        margin-left: 10px
        font-size: 14px
        letter-spacing: 0.2px
    .cost
      font-size: 14px
      letter-spacing: 0.2px
      color: #2A27C9
      font-weight: bold
      background: rgba(42, 39, 201, 0.1)
      border-radius: 4px
      padding: 6px 10px

  &-follower
    display: flex
    align-items: center
    justify-content: space-between
    margin-top: 16px
    &-number
      font-size: 14px
      color: #7780A1
      letter-spacing: 0.2px
      font-weight: 400
    button
      border: none
      background-color: transparent
</style>

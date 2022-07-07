<template>
  <div class="item">
    <div class="item-box">
      <div class="item-img">
        <img :src="item.img" alt="" />
      </div>
      <div class="item-header">
        <div class="item-header-top">
          <h3 class="item-header-title">
            {{ title }}
          </h3>
          <span class="item-header-eth">{{ cost }}</span>
        </div>
        <div class="item-header-btm">
          <div class="icon">
            <img :src="require('@/assets/icons/timer.svg')" alt="timer" />
          </div>
          <div class="time">{{ time }}</div>
        </div>
      </div>
      <hr />
      <div class="item-footer">
        <div class="item-footer-persons">
          <div class="avatar">
            <img v-for="avatar in Avatars" :key="avatar.id" alt="" :src="avatar.i" />
          </div>
        </div>
        <div class="item-footer-number">
          <span>{{ NumberPeople }} people are bidding</span>
        </div>
        <div class="item-footer-fav">
          <button @click="likeItem">
            <img
              v-if="!link"
              :src="require('@/assets/icons/heart-empty.svg')"
              alt=""
            />
            <img v-else :src="require('@/assets/icons/heart-red.svg')" alt="" />
          </button>
          <span> {{ NumberFav }} </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "slider-item",
  props: {
    image: String,
    title: String,
    cost: String,
    time: String,
    NumberFav: Number,
    NumberPeople: Number,
    Avatars: Array
  },
  data() {
    return {
      link: false,
      item: {
        img: this.image,
        title: this.title,
        cost: this.cost,
        time: this.time,
        numberFav: this.NumberFav,
        numberPeople: this.NumberPeople,
        Avatars: this.Avatars
      },
    };
  },
  methods: {
    //  like button
    likeItem: function () {
      this.link = !this.link;
      this.item.numberFav++;
      console.log(this.item.numberFav);
    },
  },
};
</script>

<style lang="sass" scoped>
.item
  position: relative
  //max-height: 400px
  margin-bottom: 30px

  &-box
    padding: 24px
    height: 100%

  &-img
    max-height: 350px
    width: 100%
    margin-bottom: 20px

    img
      border-radius: 20px
      width: 100%
      height: 100%

  &-header
    position: relative

    &-top
      display: grid
      grid-template-columns: 2.7fr 1fr
      grid-gap: 10px
      margin-bottom: 20px
      align-items: center

    &-title
      font-weight: 600
      font-size: 14px
      line-height: 25px
      text-align: left
      letter-spacing: 0.2px
      color: #060714

    &-eth
      background: rgba(42, 39, 201, 0.1)
      border-radius: 4px
      font-weight: bold
      font-size: 12px
      letter-spacing: 0.2px
      color: #2A27C9
      padding: 4px 6px

    &-btm
      text-align: left
      display: flex
      margin-bottom: 20px
      align-items: center

      .icon
        margin-right: 8px

      .time
        font-weight: 400
        font-size: 14px
        line-height: 150%
        letter-spacing: 0.2px
        color: #060714

  hr
    margin: 0 8px
    background-color: #E2E2ED
    border: 0.5px solid #E2E2ED

  &-footer
    display: grid
    margin-top: 20px
    align-items: center
    grid-template-columns: 0.7fr 1.5fr 0.5fr

    &-persons

    &-number
      span
        color: #7780A1
        letter-spacing: 0.2px
        font-weight: 400
        font-size: 10px

    &-fav
      display: flex
      align-items: center

      button
        background-color: transparent
        border: none
        width: 20px
        outline: none
        cursor: pointer
        height: 20px

        img
          width: 100%
          height: 100%

      span
        margin-left: 8px
        font-size: 12px
</style>

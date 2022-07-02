<template>
  <el-container class="intro">
    <div class="intro-coins">
      <div class="tiger coin">
        <img :src="require('@/assets/imgs/coins/tiger.svg')" alt="" />
      </div>
      <div class="eleven coin">
        <img :src="require('@/assets/imgs/coins/elev.svg')" alt="" />
      </div>
      <div class="gato coin">
        <img :src="require('@/assets/imgs/coins/fish.svg')" alt="" />
      </div>
      <div class="wolf coin">
        <img :src="require('@/assets/imgs/coins/wolf.svg')" alt="" />
      </div>
      <div class="bird coin">
        <img :src="require('@/assets/imgs/coins/bird.svg')" alt="" />
      </div>
      <div class="frog coin">
        <img :src="require('@/assets/imgs/coins/flok.svg')" alt="" />
      </div>
    </div>
    <div class="intro-background">
      <img :src="require('@/assets/imgs/circles.svg')" alt="" />
    </div>
    <div class="intro-content">
      <div class="intro-subtitle">
        <span>Non Fungible Tokens</span>
      </div>
      <div class="intro-title">
        <div class="intro-title-line first">
          <span>A new NFT</span>
          <img :src="require('@/assets/imgs/nft-right-top.svg')" alt="NFT" />
        </div>
        <div class="intro-title-line second">
          <img :src="require('@/assets/imgs/nft-left-btn.svg')" alt="NFT" />
          <span>Experience</span>
        </div>
      </div>
      <div class="intro-bottom">
        <span>Discover, collect and sell</span>
      </div>
      <SearchComponent />
      <BrandsComponent />
    </div>
  </el-container>
</template>

<script>
import SearchComponent from "@/components/search-component";
import BrandsComponent from "@/components/brands-component";
export default {
  name: "intro-section",
  components: {
    SearchComponent,
    BrandsComponent,
  },
};
</script>

<style lang="scss" scoped>
.intro {
  position: relative;
  //max-width: 1200px;
  width: 100%;
  min-height: 500px;
  margin: auto;
  display: flex;
  justify-content: center;
  &-coins {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 2;
    .coin {
      position: absolute;
      max-width: 150px;
      max-height: 150px;
      transform: translate(-50%, -50%);
      img {
        width: 100%;
      }
    }
    .tiger {
      top: 18%;
      left: 15%;
    }
    .eleven {
      top: 48%;
      left: 0%;
      //width: 150px;
    }
    .gato {
      top: 90%;
      left: 10%;
    }
    .wolf {
      top: 15%;
      right: -5%;
    }
    .bird {
      top: 50%;
      right: 5%;
    }
    .frog {
      top: 100%;
      right: -12%;
    }
  }
  &-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  &-content {
    margin-top: 50px;
    align-items: center;
    display: flex;
    z-index: 1;
    flex-direction: column;
    justify-content: center;
  }
  &-subtitle {
    font-weight: 500;
    font-size: 12px;
    line-height: 18px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: hsl(227, 18%, 55%);
    margin-bottom: 16px;
  }
  &-title {
    display: flex;
    flex-direction: column;
    .first {
      img {
        margin-left: 8px;
        width: 30px;
        height: 71px;
      }
    }
    .second {
      text-align: right;
      img {
        width: 37px;
        height: 37px;
      }
    }
    &-line {
      display: flex;
      align-items: center;
      span {
        font-weight: 600;
        font-size: 80px;
        line-height: 100%;
        letter-spacing: 0.2px;
        color: #060714;
      }
      img {
      }
    }
  }
  &-bottom {
    margin-top: 16px;
    span {
      font-size: 16px;
      font-weight: 500;
      letter-spacing: 0.2px;
      color: #7780a1;
    }
  }
}
</style>

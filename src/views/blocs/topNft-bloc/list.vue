<template>
  <div class="list">
    <div class="list-title">
      <h2>Top NFT at a lower price</h2>
    </div>
    <div class="list-items">
      <Item />
      <Item />
      <Item />
      <Item />
    </div>
    <div class="list-link">
      <el-link :underline="false" href=""> show me more </el-link>
    </div>
  </div>
</template>

<script>
import Item from "@/views/blocs/topNft-bloc/item";
export default {
  name: "list",
  components: {
    Item
  }
};
</script>

<style lang="sass" scoped>
.list
  padding: 20px
  border: 1px solid #E2E2ED
  border-radius: 20px
  &-title
    text-align: left
    padding-right: 40px
    h2
      font-size: 30px
      letter-spacing: 0.2px
      color: #060714
      line-height: 40px
      font-weight: 600
  &-items
    margin-top: 40px
    display: grid
    grid-template-columns: 1fr
    grid-gap: 10px
  &-link
    margin-top: 25px
    a
      border: 2px solid #7780A1
      border-radius: 12px
      color: #7780A1
      letter-spacing: 0.2px
      font-size: 14px
      font-weight: 600
      padding: 16px
</style>

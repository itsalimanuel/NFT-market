<template>
  <div class="top-nft">
    <List />
    <GetStart />
    <List />
  </div>
</template>

<script>
import List from "@/views/blocs/topNft-bloc/list";
import GetStart from "@/views/blocs/topNft-bloc/get-start";
export default {
  name: "index",
  components: { GetStart, List },
};
</script>

<style lang="sass" scoped>
.top-nft
  //margin-top: 50px
  display: grid
  grid-template-columns: repeat(3,1fr)
  grid-gap: 5px
  width: 1200px

  margin:
    top: 100px
    left: auto
    right: auto
    bottom: 100px
</style>

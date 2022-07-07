<template>
  <div class="auctions-slider">
    <SliderItem
      v-for="item in items"
      :key="item.id"
      :image="item.image"
      :title="item.title"
      :time="item.time"
      :cost="item.cost"
      :NumberFav="item.NumberFav"
      :NumberPeople="item.NumberPeople"
      :avatars="item.Avatars"
    />
  </div>
</template>

<script>
import SliderItem from "@/views/blocs/auctions-bloc/slider-item";
import img1 from "@/assets/imgs/nft/item-2.jpg";
import img2 from "@/assets/imgs/nft/item-4.jpg";
import img3 from "@/assets/imgs/nft/item-3.jpg";

//avatars
import avatar1 from "@/assets/avatars/01.png";
import avatar2 from "@/assets/avatars/02.png";
import avatar3 from "@/assets/avatars/03.png";

export default {
  name: "slider",
  components: { SliderItem },
  data() {
    return {
      items: [
        {
          id: "1",
          image: img1,
          title: "Vulputate felis purus viverra morbi facilisi eget",
          cost: "3.19 ETH",
          time: "2:41 min left",
          NumberFav: "35",
          NumberPeople: "120",
          Avatars: [
            { id: "1", i: avatar1 },
            { id: "2", i: avatar2 },
            { id: "3", i: avatar3 },
          ],
        },
        {
          id: "2",
          image: img2,
          title: "Dui accumsan leo vestibulum ornare eu",
          cost: "1.11 ETH",
          time: "22:59 min left",
          NumberFav: "101",
          NumberPeople: "570",
          Avatars: [
            { id: "1", i: avatar1 },
            { id: "2", i: avatar2 },
            { id: "3", i: avatar3 },
          ],
        },
        {
          id: "3",
          image: img3,
          title: "Senectus adipiscing nascetur accumsan etiam",
          cost: "1.63 ETH",
          time: "37:01 min left",
          NumberFav: "98",
          NumberPeople: "12",
          Avatars: [
            { id: "1", i: avatar1 },
            { id: "2", i: avatar2 },
            { id: "3", i: avatar3 },
          ],
        },
        {
          id: "4",
          image: img2,
          title: "Mattis at diam lorem nisl nam sed sociis",
          cost: "2.78 ETH",
          time: "12:15 min left",
          NumberFav: "98",
          NumberPeople: "5",
          Avatars: [
            { id: "1", i: avatar1 },
            { id: "2", i: avatar2 },
            { id: "3", i: avatar3 },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="sass" scoped>
.auctions-slider
  display: grid
  grid-template-columns: repeat(4, 1fr)
  grid-gap: 10px
</style>

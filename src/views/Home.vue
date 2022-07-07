<template>
  <div class="home">
    <IntroSection />
    <AuctionsBloc />
    <OverlineBloc />
    <TopNftBloc />
    <HabitantBloc />
  </div>
</template>

<script>
// @ is an alias to /src
import HabitantBloc from "@/views/blocs/habitant-bloc";
import TopNftBloc from "@/views/blocs/topNft-bloc";
import OverlineBloc from "@/views/blocs/overline-bloc";
import IntroSection from "@/views/blocs/intro-section";
import AuctionsBloc from "@/views/blocs/auctions-bloc";

export default {
  name: "Home",
  components: {
    IntroSection,
    AuctionsBloc,
    OverlineBloc,
    TopNftBloc,
    HabitantBloc
  }
};
</script>

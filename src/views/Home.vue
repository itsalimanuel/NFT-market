<template>
  <div class="home">
   <IntroSection/>
  </div>
</template>

<script>
// @ is an alias to /src
import IntroSection from "@/views/blocs/intro-section";

export default {
  name: "Home",
  components: {
    IntroSection
  },
};
</script>

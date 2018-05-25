<template>
  <section class="homepage">
     <AddConcert :addShow="addShow" />
     <Poster :concerts="concerts" />
  </section>
</template>

<script>
import AddConcert from "@/components/AddConcert";
import Posters from "@/components/Posters";

export default {
  name: "Home",
  components: {
    AddConcert,
    Posters
  }
};
</script>

<style>
.homepage {
  background-image: url("https://thumbs.dreamstime.com/b/people-clapping-night-concert-partying-raising-hands-artist-stage-blurry-aerial-view-concert-crowd-happy-57884733.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  height: 70rem;
  margin: 0px;
}
</style>

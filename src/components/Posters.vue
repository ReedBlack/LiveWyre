<template>
    <section>
        <h2>your shows</h2>
        <ul class="poster-grid">
            <Poster class="poster" :posters="posters" />
        </ul>
    </section>
</template>

<script>
import Poster from "@/components/Poster";

export default {
  name: "Posters",
  props: ["shows"],
  components: {
    Poster
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Permanent+Marker");

h2 {
  color: #b760e6;
  text-shadow: 1px 1px 1px white;
  font-family: "Permanent Marker", cursive;
}

.posters {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
}

</style>


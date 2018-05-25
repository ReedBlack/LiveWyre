<template>
    <section>
        <h2>your shows</h2>
        <ul class="poster-grid">
            <Poster class="poster" :shows="shows" />
        </ul>
    </section>
</template>

<script>
import Poster from "@/components/Poster";

export default {
  name: "Posters",
  props: ["shows", "submitConcert"],
  components: {
    Poster
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Permanent+Marker");

h2 {
  color: #b760e6;

  font-family: "Permanent Marker", cursive;
}
</style>


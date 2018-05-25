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

section {
  display: flex;
  /* height: 1000px; */
  flex-direction: column;
  align-items: center;
}

h2 {
  color: #b760e6;
  text-shadow: 2px 2px 2px white;
  font-family: "Permanent Marker", cursive;
  font-size: 10vh;
}

.poster-grid {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
  height: 1000px;
  width: 75vw;
  background-color: aquamarine;
}

</style>


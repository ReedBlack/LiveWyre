<template>
    <div class="poster">
        <li v-for="show in shows" :show="show" :key="show.artist">
            <h3>{{show.artist}}</h3>
            <small>{{show.date}}</small>
            <h4>{{show.venue}}</h4>
            <img :src="show.poster">
            <p>{{show.description}}</p>
        </li>
    </div>
</template>

<script>
export default {
  name: "poster",
  props: ["submitConcert", "shows", "show"]
};
</script>

<style>
img {
  max-height: 300px;
  max-width: 300px;
  background-size: 12%;
}
</style>
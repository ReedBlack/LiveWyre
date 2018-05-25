<template>
    <div class="poster-box">
        <li v-for="show in shows" :show="show" :key="show.artist">
            <h3>{{show.artist}}</h3>
            <small>{{show.concertDate}}</small>
            <h4>{{show.venue}}</h4>
            <img :src="show.concertPoster">
            <p>{{show.attendance}}</p>
        </li>
    </div>
</template>

<script>
export default {
  name: "poster",
  props: ["submitConcert", "shows", "show"]
};
</script>

<style scoped>
.poster-box {
  margin: 5px;
  height: 150px;
  width: 150px;
  background-color: hsl(166, 100, 45);
}
img {
  max-height: 80%;
  max-width: 80%;
  background-size: 12%;
}

li {
  list-style-type: none;
}
</style>
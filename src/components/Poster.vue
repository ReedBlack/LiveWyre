<template>
    <div class="poster-box">
        <li v-for="show in shows" :show="show" :key="show.artist">
            <img :src="show.concertPoster">
            <div class="concertInfo">
              <h3>{{show.artist}}</h3>
              <small>{{show.concertDate}}</small>
              <h4>{{show.venue}}</h4>
              <p>{{show.attendance}}</p>
            </div>
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
  height: 800px;
  width: 1000px;
  display: flex;
  flex-wrap: wrap;
}
img {
  max-height: 300px;
  max-width: auto;
  background-size: 12%;
}

li {
  list-style-type: none;
  width: 300px;
  margin: 10px;
  color: #bbb5bd;
}

.concertInfo {
  background-color: black;
  width: 200px;
  font-size: 20px;
}
</style>
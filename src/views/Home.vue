<template>
  <section class="homepage">
    <button type="button" @click.prevent="toggleForm">Add a show!</button>     
    <AddConcert :addShow="addShow" v-show="displayForm"/>
     <Posters :shows="shows" :show="show" />
  </section>
</template>

<script>
import AddConcert from "@/components/AddConcert";
import Posters from "@/components/Posters";

export default {
  name: "Home",
  data() {
    return {
      shows: [],
      displayForm: false,
      API_URL: "https://livewyre-server.herokuapp.com/"
    };
  },
  components: {
    AddConcert,
    Posters
  },
  methods: {
    addShow(show) {
      this.shows.unshift(show);
    },
    toggleForm() {
      this.displayForm = !this.displayForm;
    }
  },
  async mounted() {
    fetch(this.API_URL)
      .then(res => res.json())
      .then(res => {
        this.shows = res;
      });
  }
};
</script>

<style>
.homepage {
  background-image: url("https://thumbs.dreamstime.com/b/people-clapping-night-concert-partying-raising-hands-artist-stage-blurry-aerial-view-concert-crowd-happy-57884733.jpg");
  background-size: cover;
  width: 100%;
  background-repeat: no-repeat;
  height: 70rem;
  margin: 0px;
}
button {
  background-color: #fdb951;
  color: black;
  font-size: 30px;
  padding-top: 10px;
  padding-bottom: 10px;
  font-family: "Permanent Marker", cursive;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 20%;
}
</style>

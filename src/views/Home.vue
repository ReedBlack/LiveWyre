<template>
  <section class="homepage">
    <button type="button" @click.prevent="toggleForm">Add a show!</button>     
    <AddConcert :addShow="addShow" v-show="displayShow"/>
     <Posters :shows="shows" />
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
      displayShow: false
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
      this.displayShow = !this.displayShow;
<<<<<<< HEAD
    }
=======
    }    
>>>>>>> f5f90f5a1d97282cd9a1503b4fd0a30368fec85b
  }
};
</script>

<style>
.homepage {
  background-image: url("https://thumbs.dreamstime.com/b/people-clapping-night-concert-partying-raising-hands-artist-stage-blurry-aerial-view-concert-crowd-happy-57884733.jpg");
  background-size: contain;
  width: 100vw;
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

<template>
    <form class="concert-form" :submitConcert="submitConcert" v-on:submit.prevent="submitConcert">
        <label for="artist">Artist</label>
        <input v-model="show.artist" type="text" name="artist">
        <label for="date">Date</label>
        <input v-model="show.date" type="text" name="date">
        <label for="venue">Venue</label>
        <input v-model="show.venue" type="text" name="venue">
        <label for="poster">Poster URL</label>
        <input v-model="show.poster" type="text" name="url">
        <label for="description">Description</label>
        <textarea v-model="show.description" name="description"></textarea>
        <input type="submit" name="submit" value="Submit" />
    </form>
</template>

<script>
export default {
  name: "AddConcert",
  props: ["addShow"],
  data() {
    return {
      show: {
        artist: "",
        date: "",
        venue: "",
        poster: "",
        description: ""
      }
    };
  },
  methods: {
    submitConcert() {
      this.addShow(this.show);
      this.show = {
        artist: "",
        date: "",
        venue: "",
        poster: "",
        description: ""
      };
    }
  }
};
</script>

<style scoped>
</style>
<template>
    <form class="concert-form" :shows="shows" v-on:submit.prevent="submitConcert">
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
  props: ["addShow", "shows"],
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
<style scoped>
form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 30%;
  color: white;
  font-size: 20px;
  font-family: "Permanent Marker", cursive;
  padding: 1%;
}
input {
  width: 100%;
}
textarea {
  width: 100%;
}
#submitButton {
  background-color: #FDB951;
  color: black;
  font-size: 30px;
  padding-top: 10px;
  padding-bottom: 10px;
  font-family: "Permanent Marker", cursive;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50%;
}
</style>
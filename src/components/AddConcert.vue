<template>
    <form class="concert-form" :submitConcert="submitConcert" :shows="shows" v-on:submit.prevent="submitConcert">
        <label for="artist">Artist</label>
        <input v-model="show.artist" type="text" name="artist">
        <label for="date">Date</label>
        <input v-model="show.concertDate" type="text" name="date">
        <label for="venue">Venue</label>
        <input v-model="show.venue" type="text" name="venue">
        <label for="poster">Poster URL</label>
        <input v-model="show.concertPoster" type="text" name="url">
        <label for="attendance">Attendance</label>
        <textarea v-model="show.attendance" name="attendance"></textarea>
        <input type="submit" id="submitButton" name="submit" value="Submit" />
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
        concertDate: "",
        venue: "",
        concertPoster: "",
        attendance: ""
      },
      API_URL: "https://livewyre-server.herokuapp.com/"
    };
  },
  methods: {
    submitConcert() {
      this.addShow(this.show);
      this.postConcert();
      this.show = {
        artist: "",
        concertDate: "",
        venue: "",
        concertoster: "",
        attendance: ""
      };
    },
    postConcert() {
      return fetch(this.API_URL, {
        headers: {
          "content-type": "application/json"
        },
        method: "POST",
        body: JSON.stringify(this.show)
      });
    }
  }
};
</script>

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
  height: 550px;
}
input {
  width: 100%;
}
textarea {
  width: 100%;
}
#submitButton {
  background-color: #fdb951;
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
<template>
    <form class="concert-form" v-on:submit.prevent="submitConcert">
        <label for="artist">Artist</label>
        <input v-model="concert.artist" type="text" name="artist">
        <label for="date">Date</label>
        <input v-model="concert.date" type="text" name="date">
        <label for="venue">Venue</label>
        <input v-model="concert.venue" type="text" name="venue">
        <label for="poster">Poster URL</label>
        <input v-model="concert.poster" type="text" name="url">
        <label for="description">Description</label>
        <textarea v-model="concert.description" name="description"></textarea>
        <input type="submit" name="submit" value="Submit" />
    </form>
</template>

<script>
export default {
name: "AddConcert",
props: ['sendConcert'],
data() {
return {
    concert: {
        artist: '',
        date: '',
        venue: '',
        poster: '',
        description: ''
        }
    }
},
methods: {
    submitConcert () {
        this.sendConcert(this.concert);
        this.concert: {
            artist: '',
            date: '',
            venue: '',
            poster: '',
            description: ''
            }
        }
    }
};
</script>

<style scoped>
</style>
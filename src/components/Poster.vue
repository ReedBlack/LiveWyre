<template>
    <div>
        <li v-for="show in shows">
            <h2>{{concert.artist}}</h2>
            <small>{{concert.date}}</small>
            <h3>{{concert.venue}}</h3>
            <div>{{concert.poster}}</div>
            <p>{{concert.description}}</p>
        </li>
    </div>
</template>

<script>
export default {
  name: "poster",
  props: ["submitConcert"]
};
</script>

<style>
</style>
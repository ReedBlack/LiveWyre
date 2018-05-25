<template>
    <div>
        <li v-for="show in shows" :key="show.title">
            <h2>{{show.artist}}</h2>
            <small>{{show.date}}</small>
            <h3>{{show.venue}}</h3>
            <div>{{show.poster}}</div>
            <p>{{show.description}}</p>
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
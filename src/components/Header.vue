<template>
  <header>
    <br>&nbsp;</br>
    <br>&nbsp;</br>
    <h1 class="font">LiveWyre</h1>
  </header>
</template>

<script>
export default {
  name: "header"
};
</script>

<style scoped>

@import url("https://fonts.googleapis.com/css?family=Permanent+Marker");

header {
  display: flex;
  height: 10vh;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background-color: #9b52c2;
  margin-top: 0%;
  padding-top: 0%;
  margin-bottom: 2%;
  padding-bottom: 3%;
  border-bottom: 6px outset rgb(143, 48, 48);
}

.font {
  font-family: 'Permanent Marker', cursive;
  font-size: 20vh;
  font-weight: 200;
  color: #BBB5BD;
  padding-top: -5%;
  text-shadow: 2px 2px 2px white;

}

</style>

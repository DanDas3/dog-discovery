<template>
  <div class="container">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
    <DogFind class="center"></DogFind>
  </div>
</template>

<script>
import DogFind from "@/components/DogFind/DogFind.vue";

export default {
  name: 'App',
  components: {
    DogFind
  }
}
</script>

<style>
@import'~bootstrap/dist/css/bootstrap.css';
</style>

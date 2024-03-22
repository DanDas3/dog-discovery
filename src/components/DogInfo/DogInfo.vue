<template>
  <div >
    <div class="card-header">
      <h2 class="card-title text-center">{{ dataDog }}</h2>
    </div>
    <img class="card-img" :src="msg" alt="imagem de cachorro">

  </div>
</template>

<script>
export default {
  name: 'DogInfo',
  props: {
    msg: String,
    dataDog: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

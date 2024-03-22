<script>
import DogInfo from "@/components/DogInfo/DogInfo.vue";
import axios from "axios";
//import * as node;

export default {
  name: 'DogFind',
  data() {
    return {
      men: '',
      dogData: {},
      nameDog: ''
    }
  },
  components: {
    DogInfo
  },
  methods:{
    buscarDados() {
      axios.get(`https://dog.ceo/api/breeds/image/random`).then((res) => {
        this.dogData = res.data;
        console.log(this.dogData.message);
        this.men = this.dogData.message;
        console.log(this.men);
        this.tratarDados(this.men);
        console.log(this.nameDog);
      });
    },
    tratarDados(dado) {
      let parts = dado.split('/');
      let n = parts.length;
      this.nameDog = parts[n-2];
    }
  }
}
</script>

<template>
  <div class="card col-md-5">
    <div class="card-header">
      <h1 class="card-title text-center">Buscar por um cachorro</h1>
    </div>
    <DogInfo v-if="men !== ''" :msg="men" :data-dog="nameDog"/>
    <div class="btn btn-primary" v-on:click="buscarDados">Find dog data</div>
  </div>
</template>

<style scoped>

</style>
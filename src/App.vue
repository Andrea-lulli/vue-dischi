<template>
  <div id="app">
    <div class="box-conteiner">
      <BoxCardComp class="" v-for="(elem,index) in libreria" :key="index" :libreria="elem" />
    </div>
  </div>
</template>

<script>
import BoxCardComp from "./components/BoxCardComp.vue";
import axios from "axios";

export default {
  name: "App",
  components: {
    BoxCardComp,
  },
  data() {
    return {
      libreria: "",
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((resp) => {
        this.libreria = resp.data.response;
      });
  },
};
</script>

<style lang="scss">
#app{
  display: flex;
  justify-content: center;
}
.box-conteiner{
  width: 70%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}


</style>

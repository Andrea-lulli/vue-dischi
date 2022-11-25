<template>
  <div id="app">

    <!--  componente header -->
    <HeaderComp class="col-12" />

    <!-- conteiner card -->
    <div class="box-conteiner">
      <BoxCardComp
        class=""
        v-for="(elem, index) in libreria"
        :key="index"
        :libreria="elem"
      />
    </div>
  </div>
</template>

<script>

//importo box card
import BoxCardComp from "./components/BoxCardComp.vue";

//import axios
import axios from "axios";

//import header
import HeaderComp from "./components/HeaderComp.vue";

export default {
  name: "App",
  components: {
    BoxCardComp,
    HeaderComp,
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
#app {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  background-color: rgba(30, 45, 59, 255);
}
.box-conteiner {
  width: 70%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 50px;
  padding-bottom: 80px;
}
</style>

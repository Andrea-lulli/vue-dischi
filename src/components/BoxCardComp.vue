<template>
  <!-- componente delle card inserite in modo dinamico -->
  <div class="box-card conteiner-fluid">
    <img :src="libreria.poster" class="card-img-top" alt="..." />
    <div class="card-body">
      <p class="titolo">{{ libreria.title }}</p>
      <p class="testo">{{ libreria.author }}</p>
      <p class="testo">{{ libreria.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "BoxCardComp",
  props: {
    libreria: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div {
  img {
    width: 100%;
    aspect-ratio: 1/1;
    object-position: center;
  }
}

//boc card
.box-card {
  flex-basis: 19%;
  margin-bottom: 20px;
  background-color: rgba(46, 58, 70, 255);
  padding: 20px;
  color: white;
  text-align: center;
}

//testi delle card
.titolo {
  font-weight: 900;
  margin-top: 10px;
  font-size: 20px;
}
.testo {
  color: rgba(106, 108, 104, 255);
  line-height: 5px;
  margin: 20px 0;
}
</style>

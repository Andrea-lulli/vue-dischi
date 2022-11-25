<template>
  <div class="box-card conteiner-fluid">
    <div class="card p-4" style="">
      <img :src="libreria.poster" class="card-img-top" alt="..." />
      <div class="card-body">
        <p class="card-text">
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </p>
      </div>
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
div{
  
  img{
    width: 100%;
    aspect-ratio: 1/1;
    object-position: center;
  }
}

.box-card{
  flex-basis: 19%;
  margin-bottom: 20px;
}

</style>

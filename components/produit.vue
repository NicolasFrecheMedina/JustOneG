<template>
   <div class="col">
      <div class="card">
        <img width="auto" height="200px" :src="src" class="card-img-top" alt="">
        <div class="card-body">
          <a href="#"><h5 class="card-title"> {{ nom}} - {{ prix }} €</h5></a>
                  <p class="card-text"> {{ description }} </p>
                  <p class="card-text"><small class="text-muted fst-italic"><button @click="$emit('commande', nom, prix)" type="button" class="btn btn-outline-dark btn-sm">JoG</button></small></p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "produit",
  props: ["nom","prix","description","src"]
}
</script>

<style scoped>
img{
  opacity: 0.4;
}

a{
  text-decoration: none;
  color: black;
}
.card{
   box-shadow: 5px 5px 5px lightgrey;
}

a:hover{
  color:#198754;
}
</style>

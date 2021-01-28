<template>
    <div class="container">
      <h1 class="display-1 fst-italic">Order</h1>
      <div class="d-flex">
        <div class="shop">
          <h2>Produits disponible</h2>
          <div class="row row-cols-1 row-cols-md-3 g-4">
            <produit v-for="produit in produits" :key="produit" v-bind:nom="produit.nom" v-bind:prix="produit.prix" v-bind:description="produit.description" v-bind:src="produit.src" v-on:commande="ajouterProduit"/>
          </div>
        </div>
        <div class="panier">
          <h2>Produits commandés</h2>
          <div class="card" style="width: 18rem;">
            <ul class="list-group list-group-flush" v-for="(produit, index) in commandes" :key="produit" v-bind:nom="produit.nom" v-bind:prix="produit.prix">
              <li class="list-group-item d-flex" >
                <div class="me-auto">
                  {{produit.nom}}
                </div>
                <div>
                  {{produit.prix}} €
                </div>
                <div>
                  <a @click='removeProduit(index)' type="button" class="btn-close btn btn-outline-danger"></a>
                </div>
              </li>
            </ul>
            <div class="card-footer d-flex">
              <div class="me-auto"><strong> Total </strong></div>
              <div><strong> {{ total }} €</strong></div>
              <div><a  @click='removePanier()' type="button" class="btn-close btn btn-outline-danger"></a></div>
            </div>
          </div>
          <div class="d-flex justify-content-end mt-2">
              <button type="button" class="btn btn-outline-dark btn-sm">Order Now !</button>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import produit from '@/components/produit.vue'

export default {
  components: {
    produit
  },
  data(){
    return{
      produits : [
        { nom : 'Gorilla Glue',
          prix: 17.50,
          description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris a est nec sem sagittis varius non ornare dui vulputate ut.. Nunc auctor vel eros sed fringilla. Proin molestie enim ac pellentesque lacinia.",
          src: require('~/assets/img/tmpl5.jpg')
        },
        { nom : 'SuperLemonHaze',
          prix : 15.00,
          description: "Nulla auctor semper mauris, non ornare dui vulputate ut. Sed maximus leo et efficitur lobortis. Duis dapibus velit enim, elementum tristique metus vehicula ut. Vivamus pulvinar viverra magna quis lacinia.",
          src: require('~/assets/img/tmpl2.jpg')
        },
        { nom: 'GreenPoison',
          prix: 12.50,
          description: "Maecenas pulvinar tellus in consequat gravida. Nunc nibh tortor, ultricies in dui ac, fringilla tempor urna. Phasellus vitae ullamcorper eros. Curabitur cursus turpis ex, eget tempus metus accumsan sit amet.",
          src: require('~/assets/img/tmpl3.jpg')
        },
        { nom: 'OG Kush',
          prix: 14.50,
          description: "Etiam pellentesque est justo, accumsan porttitor massa porta malesuada. Donec elementum tortor non ornare ornare. Donec a tristique turpis. Nam fermentum iaculis tempus.",
          src: require('~/assets/img/tmpl4.jpg')
        },
        { nom: 'Critical',
          prix: 11.50,
          description: "Vestibulum blandit ornare quam vitae commodo. Vivamus pulvinar viverra magna quis lacinia. Fusce pellentesque porttitor sem, scelerisque commodo augue scelerisque ac.",
          src: require('~/assets/img/tmpl5.jpg')
        }
      ],
      commandes: [
        { nom: 'Gorilla Glue', prix: 17.50}
        ]
    }
  }, computed: {
    total(){
      return this.$data.commandes.reduce((total, produit) => total + produit.prix, 0)
    },
  },
   methods: {
      ajouterProduit(nom, prix) {
        this.$data.commandes.push({nom: nom, prix: prix})
      },
      removeProduit(index) {
         this.$data.commandes.splice(index, 1)
      },
      removePanier() {
        this.$data.commandes = []
      }
    }
}


</script>

<style scoped>
.btn-close{
  width: 5px;
  height: 5px;
  margin-left: 10px;
  margin-bottom: 2px;
}

h2{
  font-size: 30px;
}
.panier{
  margin-left: 20px;
}

</style>

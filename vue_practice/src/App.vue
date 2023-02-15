<script setup>
import landingvue from './components/landing.vue'
import componentvue from './components/component.vue'
</script>

<template>
 <landingvue/>

 <section class="results_section">

  <componentvue v-for="cake in cakes_array" :cake_obj="cake"/>

 </section>

</template>

<style scoped>

.results_section{
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
}

</style>

<script>

export default {
  data(){
    return{
      cakes_array:[
      { 
        type: 'Chocolate',
        price: 39,
        icing: 'Coffee Chocolate',
        dietary: 'Gluten Free'
      },

      { 
        type: 'Vanilla',
        price: 19,
        icing: 'Strawberry Vanilla',
        dietary: 'Vegan'
      },

      { 
        type: 'Carrot',
        price: 28,
        icing: 'Cream Cheese',
        dietary: 'Dairy Free'
      },

      { 
        type: 'Red Velvet',
        price: 59,
        icing: 'Cream Cheese Vanilla',
        dietary: 'Gluten Free'
      }
    ]

    }
  }
}
</script>
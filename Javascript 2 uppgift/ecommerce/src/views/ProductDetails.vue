<template>
  <div class="card">
      <h1>name {{product.name}}</h1>
      <p>ID: {{ product._id }}</p>
      <h3>PRICE: {{product.price}}</h3>
      <img :src="product.image" alt="" class="img">      
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  props: ['id'],
  computed: {...mapGetters(['product'])},
  methods: {...mapActions(['getProduct']) },
  created(){
    this.getProduct(this.id)
  }
}
</script>

<style scoped>
 .card{
   width: 80%;
   margin: 2rem auto;
   border: 1px solid #4b4b4b;
   border-radius: 1rem;
   padding: 1rem;
   min-height: 50vh;
 }

 .img {
   max-width: 40rem;
   display: block;
   margin: auto;
 }
</style>
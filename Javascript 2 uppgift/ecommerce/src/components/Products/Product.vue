<template>
  <div class="col">
      <div class="card p-3 img-fluid h-100">
          <img 
          :src="product.image"
          class="card-img-top" 
          alt=""
          />
          <div class="card-body">
              <h5 class="card-title">{{ product.name }}</h5>
              <p class="card-text">{{ product.short }}</p>
          </div>
          <div>
              <router-link :to="{name: 'ProductDetails', params: {id: product._id}}" type="button" class="btn btn-primary">Visa Produkt</router-link>
          </div>

      </div>
  </div>
</template>

<script>
export default {
    props: ['product']
}
</script>

<style>
.card-img-top {
    max-width: 15rem;
    margin: auto;
    max-height: 15rem;
}

.card-title {
    display: flex;
    justify-content: center;
}

.card-text {
    display: flex;
    justify-content: center;
}
</style>
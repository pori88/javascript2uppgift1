<template>
  <div class="container mt-5">
      <list/>
  </div>
</template>

<script>
import { mapActions } from 'vuex'
import List from '../components/Products/List'
export default {
    components: {
        List
    },
    methods: {
        ...mapActions(['getProducts'])
    },
    created() {
        this.getProducts()
    }
}
</script>

<style>

</style>
<template>
  <nav>
      <router-link to="/" class="logo"><i class="fas fa-truck"></i></router-link>
      <div>
          <router-link class="link" to="/" exact>Hem</router-link>
          <router-link class="link" to="/products" exact>Produkter</router-link>
          <router-link class="link" to="/about" exact>Om Oss</router-link>
      </div>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 1rem;
        background: #201d1d;
        color: #fff;
    }
    .logo {
        text-decoration: none;
        color: #fff;
        font-size: 2rem;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

    .link {
        color: #fff;
        text-decoration: none;
        padding: 1.5rem 1rem;
        display: inline-block;
        position: relative;
    }
    .link:hover {
        color: #a5a5a5
    }

    .link.router-link-active::after {
        content: '';
        position: absolute;
        border-bottom: 2px solid #00fdfd;
        left: 1rem;
        bottom: 1.3rem;
        right: 1.5rem;
    }
</style>
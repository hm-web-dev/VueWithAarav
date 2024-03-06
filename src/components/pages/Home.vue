<script>
import Header from '../Header.vue'
import Footer from '../Footer.vue'

export default {
    components: {
        Header,
        Footer
    }
}

</script>

<template>
    <p> Welcome to Home. </p>
</template>

<style scoped>

body {
  font-family: 'Lato', sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100h;
  margin: 10;
}

p {
  text-align: center;
}

</style>
<script>
import Header from './components/Header.vue'
import News from './components/pages/News.vue' // TODO: remove
import Footer from './components/Footer.vue'
import AboutUs from './components/pages/AboutUs.vue'
import Matches from './components/pages/Matches.vue'
// hi y'all, going to number the changes (there are 4) so it's clear to you. 

// 1. create a routes object with all your navbar routes
// see https://vuejs.org/guide/scaling-up/routing.html#simple-routing-from-scratch
const routes = {
  '/': null, 
  '/news': News, 
  '/about': AboutUs, 
  '/matches': Matches,
}
export default {
  data() {
    // 2. change the currentPath to be the value of the routes variable (instead of just a string)
    return {
      currentPath: routes['/']
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      // 3. remove the hash so we just get the route, and make it the currentPath 
      const removeHash = window.location.hash.slice(1);
      console.log(removeHash)
      this.currentPath = routes[removeHash || '/'];
    });
  },
  components: {
    Header,
    News,
    Footer
  }
}
</script>

<template>
  <Header />
   <!-- 4. change this to be a dynamic component, and add :is="currentPath" as a directive -->
   <component :is="currentPath" />
  <Footer />
</template>

<style>
</style>

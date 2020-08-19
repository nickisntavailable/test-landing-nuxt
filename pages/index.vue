<template>
  <section>
    <Appinfo />
    <Benefits />
    <Usage />
    <Footer />
  </section>
</template>

<script>
import Appinfo from '../components/Appinfo.vue';
import Benefits from '../components/Benefits.vue';
import Usage from '../components/Usage.vue';
import Footer from '../components/Footer.vue';

export default {
  components: {
    Appinfo,
    Benefits,
    Usage, 
    Footer
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}


</style>


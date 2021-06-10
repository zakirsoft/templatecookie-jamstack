<template>
  <div>
    <site-header></site-header>
    <Nuxt />
    <site-footer></site-footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
export default {
    components: {
        'site-header': Header,
        'site-footer': Footer,
    }
}
</script>

<style lang="scss">
    @import '~assets/scss/main.scss';
    @import '~bootstrap/scss/bootstrap.scss';
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');
</style>

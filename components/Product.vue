<template>
    <div class="filter--card">
        <div class="filter--card--img">
            <nuxt-link :to="{ name: 'product-slug', params: {slug: product.slug} }">
                <img :src="'https://templatecookie-nuxt.netlify.app' + product.thumbnail" class=" filter--card--img" alt="...">
            </nuxt-link>
            <div class="filter--card--overlay text-center">
                <a :href="product.link" target="_blank">Preview</a>
                <a :href="product.purhcase" target="_blank" v-if="product.price > 0">Purchase</a>
                <a :href="product.download" target="_blank" v-else>Download</a>
            </div>
        </div>
        <div class="filter--card--body">
            <a class="cat" href="#">{{ product.product_category }}</a>
            <nuxt-link :to="{ name: 'product-slug', params: {slug: product.slug } }" class="d-block">
                <h5 class="card-title">{{ product.title }}</h5>
            </nuxt-link>
            <div class="filter--card--body--footer align-items-center">
                <span class="card-text-left">${{ product.price }}</span>
                <span class="card-text-right">
                    <span class="figure">
                        <download />
                    </span> 
                    <span class=" card-text-right--number">2.4k</span>
                </span>
            </div>
        </div>
    </div>
</template>

<script>
import Download from "./svg/Download.vue"

export default {
  props: ['product'],
  components: {
      Download,
  }
}
</script>

<style>

</style>

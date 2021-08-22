<template>
    <div>
        <!-- details banner Section start-->
        <section class="details details--banner">
            <div class="details" :style="'background-image: url('+ require('~/assets/images/details-banner.png') +')'">
                <div class="container">
                    <div class="row ">
                        <div class="col-md-12 col-lg-6 align-self-center  order2">
                            <div class="details--content">
                                <div class="details--content--breadcumbs">
                                    <span class="home-breadcumbs">
                                        <home />
                                    </span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="default-breadcumbs">Categories</span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="xtra_color default-breadcumbs">{{ category.title }}</span>
                                </div>
                                <h3>{{ category.title }}</h3>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!--  filter-template Section start-->
        <section class="filter-template" style="padding-top: 100px">
            <div class="container  filter-template--box">
                <!--  item-->
                <div class="row">
                    <div class="col-md-6 col-lg-3 col-sm-6" v-for="product in products" :key="product.slug">
                        <product :product="product"/>
                    </div>
                </div>
                <div class="mt-5 text-center">
                    <button type="submit" class="details--content__button">
                        Buy Now  
                        <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" viewBox="0 0 256 256"><rect width="256" height="256" fill="none"></rect><polyline points="176.167 99.716 224.167 99.716 224.167 51.716" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="20"></polyline><path d="M190.2254,190.2254a88,88,0,1,1,0-124.4508l33.94112,33.94113" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="20"></path></svg>
                    </button>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
import Home from '~/components/svg/Home.vue'
export default {
  components: { Home },
  async asyncData ({ $content, params }) {
    const category = await $content('/categories', params.slug)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Category not found' })
      })

    const products = await $content('/products').where({ product_category: category.title})
      .sortBy('createdAt', 'desc')
      .limit(8)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Something went wrong, Please try again!' })
      })
    return { category, products }
  },
}
</script>

<style>

</style>

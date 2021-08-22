<template>
  <div>
    <!--  banner Section start-->
    <section class=" header" id="header">
        <div class="banner" :style="'background-image: url('+ require('~/assets/images/banner-background.png') +')'">
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-md-7 ">
                        <div class="banner--content">
                            <h2>Premium UI &<br> HTML Template.</h2>
                            <p>
                                Quisque sed est condimentum, placerat tellus a, dictum diam. Praesent volutpat<br> nisl
                                ac ligula
                                lobortis imperdiet. Aenean in est mattis.
                            </p>
                            <!-- <form>
                                <div class="form-group banner--content--form justify-content-center">
                                    <input type="email" class="form-control banner--content__searchbar"
                                        id="exampleInputEmail1" aria-describedby="emailHelp"
                                        placeholder="Botstrap, figma, html etc...">
                                    <button type="submit" class="banner--content__button">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M7.33333 12.6667C10.2789 12.6667 12.6667 10.2789 12.6667 7.33333C12.6667 4.38781 10.2789 2 7.33333 2C4.38781 2 2 4.38781 2 7.33333C2 10.2789 4.38781 12.6667 7.33333 12.6667Z"
                                                stroke="white" stroke-width="0.75" stroke-linecap="round"
                                                stroke-linejoin="round" />
                                            <path d="M14.0001 14L11.1001 11.1" stroke="white" stroke-width="0.75"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                        <span>Search</span>
                                    </button>
                                </div>
                            </form> -->
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!--  filter-template Section start-->
    <section id="filter-template" class="filter-template">
        <div class="container  filter-template--box">
            <div class="row justify-content-center">
                <div class="col-lg-7 col-md-9 text-center">
                    <div class="filter-template-menu-item">
                        <ul>
                            <li><a href="#" class="active">All Template</a></li>
                            <li v-for="category in categories" :key="category.slug"><a href="#">{{ category.title }}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <!--  item-->
            <div class="row">
                <div class="col-md-6 col-lg-3 col-sm-6" v-for="product in products" :key="product.id">
                    <product :product="product" />
                </div>
            </div>
        </div>
    </section>

    <!--  Newest template Section start-->
    <!-- <slider-section :products="products" :slidesPerView="5"  title="Newest Template" :bgImage="require('~/assets/images/newest-background.png')"></slider-section> -->
    <!-- <section class="newest" :style="'background-image: url('+ require('~/assets/images/newest-background.png') +')'">
        <div class="container">
            <div class="newest--header">
                <div class="newest--header--title">
                    <h3>Newest Template</h3>
                </div>
                <div class="newest--header--arrow">
                    <span>
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M20.25 12H3.75" stroke="white" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" />
                            <path d="M10.5 5.25L3.75 12L10.5 18.75" stroke="white" stroke-width="2"
                                stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </span>
                    <span class="after-line">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M3.75 12H20.25" stroke="white" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" />
                            <path d="M13.5 5.25L20.25 12L13.5 18.75" stroke="white" stroke-width="2"
                                stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                    </span>
                </div>
            </div>

            <div class="row">
                <div class="col-md-6  col-lg-3 col-sm-6">
                    <product />
                </div>
                <div class="col-md-6  col-lg-3 col-sm-6">
                    <product />
                </div>
                <div class="col-md-6  col-lg-3 col-sm-6">
                    <product />
                </div>
                <div class="col-md-6  col-lg-3 col-sm-6">
                    <product />
                </div>
            </div>
        </div>
    </section> -->
    
    <!--  free Template  Section start-->
    <!-- <section class="featured">
        <div class="container">
            <div class="row">
                <div class="col-md-12">
                    <div class="featured--header">
                        <div class="newest--header--title ">
                            <h3 class="text-center">Featured Template</h3>
                        </div>
                    </div>
                </div>
            </div>

            <div class="row">
                <div class="col-md-6 col-lg-4 col-sm-6">
                    <product />
                </div>
                <div class="col-md-6 col-lg-4 col-sm-6">
                    <product />
                </div>
                <div class="col-md-6 col-lg-4 col-sm-6">
                    <product />
                </div>
            </div>
        </div>
    </section> -->

    <!--  free template Section start-->
    <!-- <slider-section :products="products" :slidesPerView="5" title="Free Template"></slider-section> -->
  </div>
</template>

<script>
import Product from '@/components/Product.vue'
import SliderSection from '~/components/SliderSection.vue'

export default {
  components: {
    Product,
    SliderSection
  },
  async asyncData ({ $content, params }) {
    const products = await $content('/products', params.slug)
      .sortBy('createdAt', 'desc')
      .limit(8)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Something went wrong, Please try again!' })
      })
    const categories = await $content('/categories', params.slug)
      .sortBy('createdAt', 'desc')
      .limit(8)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Something went wrong, Please try again!' })
      })

    return { products, categories }
  },
  data(){
      return {
          products: [
              {
                  id: 1,
                  title: 'Product title goes here 1',
                  price: 95
              },
              {
                  id: 2,
                  title: 'Product title goes here 2',
                  price: 63
              },
              {
                  id: 3,
                  title: 'Product title goes here 3',
                  price: 92
              },
              {
                  id: 4,
                  title: 'Product title goes here 4',
                  price: 29
              },
              {
                  id: 5,
                  title: 'Product title goes here 5',
                  price: 68
              },
              {
                  id: 6,
                  title: 'Product title goes here 6',
                  price: 12
              },
              {
                  id: 7,
                  title: 'Product title goes here 7',
                  price: 46
              },
              {
                  id: 8,
                  title: 'Product title goes here 8',
                  price: 8
              },
          ]
      }
  },
  methods: {
    // onSwiper(swiper) {
    //   alert(swiper);
    // },
    // onSlideChange() {
    //   alert('slide change');
    // },
  }
}
</script>

<style>

</style>

<template>
    <div>
        <!-- <nuxt-content :document="product"/>
        <hr>
        <code>
            <pre>
                 {{ product }}
            </pre>
        </code> -->
        
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
                                    <span class="default-breadcumbs">Product</span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="default-breadcumbs">{{ product.productCategory }}</span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="xtra_color default-breadcumbs">{{ product.title }}</span>
                                </div>
                                <h3>{{ product.title }}</h3>
                                <p class="my-3">${{product.price}}.00 <span>MIT Licenses</span></p>
                                <button type="submit" class="details--content__button">
                                    Buy Now
                                </button>
                                <button type="submit" class="details--content__button xtra_btn">
                                    Live Preview
                                </button>
                            </div>
                        </div>
                        <div class="col-md-12 col-lg-6  order1">
                            <div class="details--img">
                                <img :src="product.thubmnail" alt="">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <div class="bg-white" style="padding: 50px 0;">
            <section class="description">
                <div class="container">
                    <div class="row">
                        <div class="col-md-12 col-lg-8">
                            <div class="description--header">
                                <h3>Description</h3>
                            </div>
                            <div class="description--content">
                              {{ product.description }}
                               <nuxt-content :document="product"/>
                            </div>
                        </div>
                        <div class="col-md-12 col-lg-4">
                            <div class="card">
                                <div class="card--header">
                                    <div class="brand">
                                        <span> Made with: </span>
                                        <a href="#"> <img src="~/assets/images/figma.png" alt=""> </a>
                                        <a href=""> <img src="~/assets/images/xd.png" alt=""> </a>
                                    </div>
                                    <div class="price">
                                        <div class="price__left">
                                            <span>
                                                <cart />
                                            </span>
                                            <span>157 Purchases</span>
                                        </div>
                                        <div class="price__right">
                                            <span class="price_color">Price:</span> <span>$59.00</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="card--description">
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <reload />
                                            </span> 
                                            <span>Last Update:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>1 months ago</span>
                                        </div>
                                    </div>
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <sound />
                                            </span>
                                            <span>Released:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>2 years ago </span>
                                        </div>
                                    </div>
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <version />
                                            </span>
                                            <span>Version:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>2.7.4</span>
                                        </div>
                                    </div>
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <list />
                                            </span>
                                            <span>Category:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>UI Template</span>
                                        </div>
                                    </div>
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <docs />
                                            </span>
                                            <span>Documentation:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>Well Documentation</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <section class="template--feature">
                <div class="container">
                    <div class="row">
                        <div class="col-md-12">
                            <div class="template--feature--header">
                                <h3>Template Feature</h3>
                            </div>
                            <div class="template--feature-item" v-for="item in product.template_feature" :key="item.title">
                                <li>
                                  <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> 
                                    <span>{{ item.title }}</span>
                                </li>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!--  Newest template Section start-->
        <slider-section :products="products" :slidesPerView="4" title="Related Template"></slider-section>
    </div>
</template>

<script>
import SliderSection from '~/components/SliderSection.vue';
import Cart from '~/components/svg/Cart.vue';
import Docs from '~/components/svg/Docs.vue';
import Home from '~/components/svg/Home.vue';
import List from '~/components/svg/List.vue';
import LoadMore from '~/components/svg/LoadMore.vue';
import Reload from '~/components/svg/Reload.vue';
import Sound from '~/components/svg/Sound.vue';
import Version from '~/components/svg/Version.vue';

export default {
  components: {
    SliderSection,
    LoadMore,
    Cart,
    Version,
    List,
    Docs,
    Sound,
    Reload,
    Home,
  },
  head(){
    return {
      title: this.product.title,
      meta: [
        { hid: 'description', name: 'description', content: this.product.description },
        // Open Graph
        { hid: 'og:title', property: 'og:title', content: this.product.title },
        { hid: 'og:image', property: 'og:image', content: this.product.thumbnail },
        { hid: 'og:description', property: 'og:description', content: this.product.description },
        // Twitter Card
        { hid: 'twitter:title', name: 'twitter:title', content: this.product.title },
        { hid: 'twitter:description', name: 'twitter:description', content: this.product.description }
      ]
    }
  },
  async asyncData ({ $content, params }) {
    const product = await $content('/products', params.slug)
    .fetch()
    .catch(err => {
        error({ statusCode: 404, message: "Page not found" });
    });
    return { product }
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
  }
}
</script>

<style>

</style>

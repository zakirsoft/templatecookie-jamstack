<template>
    <!--  free template Section start-->
    <!-- :style="'background-image: url('+ require('~/assets/images/newest-background.png') +')'" -->
    <section class="newest" :class="bgImage ? '' : 'free'" :style="bgImage ? 'background-image: url('+ bgImage +')' : ''">
      <div class="container">
        <div class="newest--header ">
          <div class="newest--header--title">
            <h3>{{ title }}</h3>
          </div>
          <div class="newest--header--arrow">
            <span class="left-arrow" :class="leftArrowClass">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M20.25 12H3.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M10.5 5.25L3.75 12L10.5 18.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
              </svg>
            </span>
            <span class="after-line right-arrow" :class="rightArrowClass">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M3.75 12H20.25" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M13.5 5.25L20.25 12L13.5 18.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
              </svg>
            </span>
          </div>
        </div>
        <client-only>
            <div v-swiper="swiperOption" :loadtheme="false">
                <div class="swiper-wrapper">
                    <div class="swiper-slide" :key="item.id" v-for="item in products">
                        <product :product="item" />
                    </div>
                </div>
            </div>
        </client-only>
      </div>
    </section>
</template>

<script>
export default {
  name: "Slider",
  props: {
    title: String,
    products: Array,
    slidesPerView: Number,
    bgImage: {
      type: String,
      default: null,
    }
  },
  data() {
    return {
      leftArrowClass: '',
      rightArrowClass: '',
      swiperOption: {
        slidesPerView: this.slidesPerView,
        spaceBetween: 10,
        slidesPerGroup: 1,
        loop: true,
        // loopFillGroupWithBlank: true,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        navigation: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: this.rightArrowClass,
          prevEl: this.leftArrowClass,
        },
        breakpoints: {
            1024: {
              slidesPerView: 3,
              spaceBetween: 10
            },
            768: {
              slidesPerView: 3,
              spaceBetween: 10
            },
            640: {
              slidesPerView: 2,
              spaceBetween: 10
            },
            320: {
              slidesPerView: 1,
              spaceBetween: 10
            }
          }
      },
    };
  },
  created(){
    let arrowClass = this.title.toLowerCase().replace(" ", "-");

    this.leftArrowClass = 'left-' + arrowClass + 'slider-arrow'
    this.rightArrowClass  = 'right-' + arrowClass + 'slider-arrow';
  },
};
</script>

<style scoped>

</style>

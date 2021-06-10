<template>
    <!--  free template Section start-->
    <section class="newest free">
      <div class="container">
        <div class="newest--header ">
          <div class="newest--header--title">
            <h3>Free Template</h3>
          </div>
          <div class="newest--header--arrow">
            <span class="left-arrow">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M20.25 12H3.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M10.5 5.25L3.75 12L10.5 18.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
              </svg>
            </span>
            <span class="after-line right-arrow">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M3.75 12H20.25" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M13.5 5.25L20.25 12L13.5 18.75" stroke="white" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
              </svg>
            </span>
          </div>
        </div>
        <div v-swiper="swiperOption" :loadtheme="false">
          <div class="swiper-wrapper">
            <div class="swiper-slide" :key="item" v-for="item in products">
              <product :product="item" />
            </div>
          </div>
        </div>
      </div>
    </section>
</template>

<script>
import { directive } from "vue-awesome-swiper";

export default {
  name: "Slider",
  props: ['products'],
  directives: {
    swiper: directive,
  },
  data() {
    return {
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 10,
        slidesPerGroup: 3,
        loop: true,
        // loopFillGroupWithBlank: true,
        autoplay: {
          delay: 2500,
          disableOnInteraction: false
        },
        // pagination: {
        //   el: ".swiper-pagination",
        //   clickable: true,
        // },
        navigation: {
          nextEl: ".right-arrow",
          prevEl: ".left-arrow",
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
};
</script>

<style scoped>

</style>

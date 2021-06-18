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
                                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M16.875 16.875V9.02642C16.875 8.93934 16.8568 8.85322 16.8216 8.77358C16.7863 8.69395 16.7349 8.62255 16.6704 8.56397L10.42 2.88154C10.3049 2.77694 10.155 2.71899 9.99955 2.71899C9.84406 2.719 9.69415 2.77696 9.57911 2.88157L3.32954 8.56397C3.26511 8.62255 3.21364 8.69395 3.17842 8.77358C3.14319 8.85321 3.125 8.93932 3.125 9.0264V16.875"
                                                stroke="#6E7980" stroke-width="1.5" stroke-linecap="round"
                                                stroke-linejoin="round" />
                                            <path d="M1.25 16.875H18.75" stroke="#6E7980" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                            <path
                                                d="M11.8745 16.8744V12.4994C11.8745 12.3336 11.8087 12.1747 11.6915 12.0574C11.5742 11.9402 11.4153 11.8744 11.2495 11.8744H8.74951C8.58375 11.8744 8.42478 11.9402 8.30757 12.0574C8.19036 12.1747 8.12451 12.3336 8.12451 12.4994V16.8744"
                                                stroke="#6E7980" stroke-width="1.5" stroke-linecap="round"
                                                stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="default-breadcumbs">Category</span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="xtra_color default-breadcumbs">Category</span>
                                </div>
                                <h3>Category Page</h3>
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
                    <div class="col-md-6  col-lg-3 col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3 col-sm-6">
                        <product />
                    </div>
                    <div class="col-md-6 col-lg-3  col-sm-6">
                        <product />
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
export default {

}
</script>

<style>

</style>

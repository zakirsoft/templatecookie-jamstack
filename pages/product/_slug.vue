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
                                    <span class="default-breadcumbs">Product</span>
                                    <span class="default-breadcumbs">
                                        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path d="M5.5 3L10.5 8L5.5 13" stroke="#8A9399" stroke-width="1.5"
                                                stroke-linecap="round" stroke-linejoin="round" />
                                        </svg>
                                    </span>
                                    <span class="default-breadcumbs">Figma</span>
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
                                <p class="my-3">$59.00 <span>MIT Licenses</span></p>
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
                                <img src="~/assets/images/image.jpg" alt="">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <div class="bg-white" style="padding: 50px 0;">
            <!-- Description banner Section start -->
            <section class="description">
                <div class="container">
                    <div class="row">
                        <div class="col-md-12 col-lg-8">
                            <div class="description--header">
                                <h3>Description</h3>
                            </div>
                            <div class="description--content">
                               <nuxt-content :document="product"/>
                            </div>
                        </div>
                        <div class="col-md-12 col-lg-4">
                            <div class="card">
                                <div class="card--header">
                                    <duv class="brand">
                                        <span>Made with:</span>
                                        <a href="#"><img src="~/assets/images/figma.png" alt=""></a>
                                        <a href=""> <img src="~/assets/images/xd.png" alt=""></a>


                                    </duv>
                                    <div class="price">
                                        <div class="price__left">
                                            <span>
                                                <svg width="32" height="32" viewBox="0 0 32 32" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path opacity="0.2"
                                                        d="M7.81818 18H23.5127C23.981 18 24.4346 17.8356 24.7942 17.5355C25.1538 17.2354 25.3966 16.8186 25.4804 16.3578L27 8H6L7.81818 18Z"
                                                        fill="#0080FF" />
                                                    <path
                                                        d="M23 23H8.72727L5.2402 3.82112C5.19831 3.5907 5.07688 3.3823 4.89708 3.23225C4.71728 3.08219 4.49052 3 4.25633 3H2"
                                                        stroke="#0080FF" stroke-width="2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M10 28C11.3807 28 12.5 26.8807 12.5 25.5C12.5 24.1193 11.3807 23 10 23C8.61929 23 7.5 24.1193 7.5 25.5C7.5 26.8807 8.61929 28 10 28Z"
                                                        stroke="#0080FF" stroke-width="2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M23 28C24.3807 28 25.5 26.8807 25.5 25.5C25.5 24.1193 24.3807 23 23 23C21.6193 23 20.5 24.1193 20.5 25.5C20.5 26.8807 21.6193 28 23 28Z"
                                                        stroke="#0080FF" stroke-width="2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M7.81818 18H23.5127C23.981 18 24.4346 17.8356 24.7942 17.5355C25.1538 17.2354 25.3966 16.8186 25.4804 16.3578L27 8H6"
                                                        stroke="#0080FF" stroke-width="2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                </svg>
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
                                                <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M13.7631 7.79034H17.5131V4.04034" stroke="#A2AAB0"
                                                        stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" />
                                                    <path
                                                        d="M5.13867 5.13864C5.77707 4.50024 6.53497 3.99383 7.36908 3.64833C8.2032 3.30283 9.09719 3.125 10 3.125C10.9029 3.125 11.7969 3.30283 12.631 3.64833C13.4651 3.99383 14.223 4.50024 14.8614 5.13864L17.513 7.79029"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path d="M6.23694 12.2097H2.48694V15.9597" stroke="#A2AAB0"
                                                        stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round" />
                                                    <path
                                                        d="M14.8613 14.8614C14.2229 15.4998 13.465 16.0062 12.6309 16.3517C11.7968 16.6972 10.9028 16.875 9.99995 16.875C9.09711 16.875 8.20311 16.6972 7.369 16.3517C6.53489 16.0062 5.77699 15.4998 5.13859 14.8614L2.48694 12.2097"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                </svg>
                                            </span> <span>Last Update:</span>
                                        </div>
                                        <div class="card--description__right">
                                            <span>1 months ago</span>
                                        </div>
                                    </div>
                                    <div class="card--description--item">
                                        <div class="card--description__left">
                                            <span>
                                                <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path
                                                        d="M8.125 6.25V15.9155C8.125 16.0184 8.0996 16.1197 8.05105 16.2104C8.0025 16.3011 7.9323 16.3785 7.84669 16.4355L6.98793 17.008C6.90459 17.0636 6.80913 17.0983 6.70957 17.1093C6.61001 17.1202 6.50928 17.1071 6.41587 17.071C6.32245 17.0349 6.23908 16.9768 6.17278 16.9017C6.10648 16.8267 6.05919 16.7368 6.0349 16.6396L5 12.5"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M5 12.5C4.1712 12.5 3.37634 12.1708 2.79029 11.5847C2.20424 10.9987 1.875 10.2038 1.875 9.37501C1.875 8.5462 2.20424 7.75135 2.79029 7.1653C3.37634 6.57925 4.1712 6.25001 5 6.25001H8.125C8.125 6.25001 12.379 6.25001 16.4727 2.8166C16.5638 2.73997 16.6748 2.69093 16.7928 2.67525C16.9107 2.65957 17.0307 2.6779 17.1386 2.72808C17.2465 2.77826 17.3379 2.85821 17.4019 2.95853C17.4659 3.05884 17.4999 3.17535 17.5 3.29435V15.4557C17.4999 15.5747 17.4659 15.6912 17.4019 15.7915C17.3379 15.8918 17.2465 15.9718 17.1386 16.0219C17.0307 16.0721 16.9107 16.0904 16.7928 16.0748C16.6748 16.0591 16.5638 16.01 16.4727 15.9334C12.379 12.5 8.125 12.5 8.125 12.5H5Z"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                </svg>
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
                                                <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path
                                                        d="M15.3127 16.875C16.5209 16.875 17.5002 15.8956 17.5002 14.6875C17.5002 13.4794 16.5209 12.5 15.3127 12.5C14.1046 12.5 13.1252 13.4794 13.1252 14.6875C13.1252 15.8956 14.1046 16.875 15.3127 16.875Z"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M15.3127 12.5L15.3126 9.36571C15.3125 8.3712 14.9174 7.41744 14.2142 6.71421L11.25 3.75"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path d="M11.25 6.875V3.75H14.375" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path
                                                        d="M4.6875 7.5C5.89562 7.5 6.875 6.52062 6.875 5.3125C6.875 4.10438 5.89562 3.125 4.6875 3.125C3.47938 3.125 2.5 4.10438 2.5 5.3125C2.5 6.52062 3.47938 7.5 4.6875 7.5Z"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path
                                                        d="M4.6875 7.5L4.68763 10.6343C4.68767 11.6288 5.08275 12.5826 5.78598 13.2858L8.75019 16.25"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path d="M8.75012 13.125V16.25H5.62512" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                </svg>

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
                                                <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M7.5 5H16.875" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M7.50049 10H16.875" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M7.50049 15H16.875" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M3.125 5H4.375" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M3.12549 10H4.37501" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M3.12549 15H4.37501" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                </svg>
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
                                                <svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                                    xmlns="http://www.w3.org/2000/svg">
                                                    <path
                                                        d="M15.625 17.5H4.37439C4.20863 17.5 4.04966 17.4342 3.93245 17.3169C3.81524 17.1997 3.74939 17.0408 3.74939 16.875V3.125C3.74939 2.95924 3.81524 2.80027 3.93245 2.68306C4.04966 2.56585 4.20863 2.5 4.37439 2.5H11.875L16.25 6.875V16.875C16.25 16.9571 16.2338 17.0383 16.2024 17.1142C16.171 17.19 16.125 17.2589 16.0669 17.3169C16.0089 17.375 15.94 17.421 15.8642 17.4524C15.7883 17.4838 15.7071 17.5 15.625 17.5Z"
                                                        stroke="#A2AAB0" stroke-width="1.2" stroke-linecap="round"
                                                        stroke-linejoin="round" />
                                                    <path d="M11.875 2.5V6.875H16.2506" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M7.5 10.625H12.5" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                    <path d="M7.5 13.125H12.5" stroke="#A2AAB0" stroke-width="1.2"
                                                        stroke-linecap="round" stroke-linejoin="round" />
                                                </svg>

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
                    <code>
                      <pre>
                        {{ product }}
                      </pre>
                    </code>
                </div>
            </section>

            <!--  template description start-->
            <section class="template--feature">
                <div class="container">
                    <div class="row">
                        <div class="col-md-12">
                            <div class="template--feature--header">
                                <h3>Template Feature</h3>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>40+ High-quality Screens in Figma Template.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>3 Different & Unique Home Screens.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Easily Customizable Figma Files.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>All Layers, Groups, and Components are Logically Named Correctly.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Perfect for Convert into HTML, WordPress, Joomla, and others Computer
                                        Languages.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Based on Bootstrap 1170px Grid System.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Full Width 1920px.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Pixel Perfect Design.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Freepik & Unsplash Images Used.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Free Google Fonts Used. (Poppins)</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>Icon Provided by Flaticon & Feather. (flat icon)
                                    </span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>40+ High-quality Screens in Figma Template.</span>
                                </li>
                            </div>
                            <div class="template--feature-item">
                                <li><svg width="20" height="20" viewBox="0 0 20 20" fill="none"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <path d="M16.875 5.6254L8.125 14.375L3.75 10.0004" stroke="#0FAC1F" stroke-width="2"
                                            stroke-linecap="round" stroke-linejoin="round" />
                                    </svg> <span>100% High-quality Screens in Figma Template.</span>
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

export default {
  components: {
    SliderSection
  },
  async asyncData ({ $content, params }) {
    const product = await $content('/products', params.slug)
      .sortBy('createdAt', 'desc')
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Product not found' })
      })
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

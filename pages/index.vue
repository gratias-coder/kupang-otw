<template>
  <div>
    <!-- <NavTwo /> -->
    <section class="slider-one">
      <div class="slider-one__carousel">
        <swiper :options="swiperOptions">
          <swiper-slide>
            <div
              class="item slider-one__slider-1"
              style="background-image: url(/images/home2-slidebg-2.jpg)"
            >
              <div
                class="container slider__content"
                style="text-align: center"
              ></div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </section>

    <section
      v-observe-visibility="onVisibilityChange"
      class="offer-area responsive-content inspire-area area-padding"
    >
      <div class="offer-fluid">
        <div class="container">
          <div class="row offer-content">
            <div class="inspire-list-box">
              <div class="inspire-img mb-30px"></div>
              <!-- end inspire-img -->
              <div class="story-content">
                <div class="top-story">
                  <span class="fontello icon-achievement success__icon"></span>
                  <span class="story__numbr counter">
                    <countTo
                      :startVal="0"
                      :endVal="startCounter ? 98903 : 0"
                      :duration="3000"
                    ></countTo>
                  </span>
                  <span class="story__numbr">+</span>
                </div>
                <!-- end top-story -->
                <p class="success__desc">
                  client success stories by the help of avivon
                </p>
              </div>
              <!-- end story-content -->
            </div>
            <!-- end col-md-6 -->
            <div class="offer-list-box">
              <div class="offer-list">
                <div class="avivon-heading">
                  <h2 class="avivon__title inspire-title">
                    Tentang Gereja Santo Petrus <br />
                    Kupang, NTT
                  </h2>
                  <p class="avivon__desc mt-45px mb-40px">
                    we inspire and help our customers expand their markets there
                    are many variations of passages of lorem ipsum is simply
                    free text available but majority have suffered alteration in
                    some area that is not form by injected humour or randomised
                    words don’t know which don't look even slightly believable.
                  </p>
                  <a href="#" class="get__btn"
                    >selengkapnya
                    <span class="fontello icon-angle-double-right"></span>
                  </a>
                </div>
                <!-- end avivon-heading -->
              </div>
              <!-- end offer-list -->
            </div>
            <!-- end offer-list-box -->
          </div>
          <!-- end row -->
        </div>
        <!-- container-fluid -->
      </div>
      <!-- end offer-fluid -->
    </section>

    <section
      class="
        ofc-caoursel-area
        responsive-content
        recent-area
        cases-area
        area-padding
        case-page-1
      "
    >
      <div class="ofc-caoursel-fluid">
        <div class="container">
          <div class="row mb-30px masonary-layout">
            <div class="avivon-heading mb-30px">
              <h2 class="avivon__title">Pengumuman</h2>
            </div>
            <!-- end col-md-12 -->
            <div class="masonary-item">
              <div class="case-list">
                <div class="office-list-item">
                  <div class="office__name">
                    <span class="office__desc-top">Pengumuman 1</span>
                    <h3 class="office__name-title">
                      <nuxt-link to="/single-cases">Isi pengumuman</nuxt-link>
                    </h3>
                  </div>
                  <!-- end office__name -->
                  <div class="recent__btn">
                    <nuxt-link to="/single-cases" class="recent__btn-btn">
                      Selengkapnya
                      <span class="fontello icon-angle-double-right"></span>
                    </nuxt-link>
                  </div>
                </div>
                <!-- end office-list-item -->
              </div>
              <!-- end office-list -->
            </div>
            <!-- end col-md-3 -->
          </div>
          <!-- end row -->
        </div>
        <!-- container -->
      </div>
      <!-- end blog-fluid -->
    </section>

    <section
      class="
        ofc-caoursel-area
        responsive-content
        recent-area
        cases-area
        area-padding
        case-page-1
      "
    >
      <div class="ofc-caoursel-fluid">
        <div class="container">
          <div class="row mb-30px masonary-layout">
            <div class="avivon-heading mb-30px">
              <h2 class="avivon__title">Kolekte</h2>
            </div>
            <!-- end col-md-12 -->
            <div class="masonary-item">
              <div class="case-list">
                <div class="office-list-item">
                  <div class="office__name">
                    <span class="office__desc-top">Kolekte </span>
                    <h3 class="office__name-title">
                      <span v-for="(item, i) in dataKolekte" :key="i" :item="item">{{item.kolekte}}</span>
                    </h3>
                  </div>
                  <!-- end office__name -->
                </div>
                <!-- end office-list-item -->
              </div>
              <!-- end office-list -->
            </div>
            <!-- end col-md-3 -->
          </div>
          <!-- end row -->
        </div>
        <!-- container -->
      </div>
      <!-- end blog-fluid -->
    </section>
    <Blog />
    <!-- <Meet /> -->
    <Footer />
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
import countTo from "vue-count-to";
import { ObserveVisibility } from "vue-observe-visibility";
import Footer from "../components/Footer";
import Blog from "../components/Blog";

export default {
  components: {
    Swiper,
    SwiperSlide,
    countTo,
    Footer,
    Blog,
  },

  directives: {
    swiper: directive,
    ObserveVisibility,
  },

 

  data : () => ({
    
  
      swiperOptions: {
        slidesPerView: 1,
        loop: false,
        speed: 1000,
        spaceBetween: 30,
        autoplay: {
          delay: 3000,
          disableOnInteraction: false,
        },
        pagination: {
          el: ".swiper-pagination",
          type: "bullets",
          clickable: true,
        },
        dataKolekte: [
          {
            kolekte: "Isi Kolekte"
          },
        ],
      },
    
  }),
  mounted() {
    MediaBox(".mediabox");
  },
  methods: {
    onVisibilityChange(isVisible) {
      if (isVisible) {
        this.startCounter = true;
      }
    },
  },
};
</script>

<style>
</style>

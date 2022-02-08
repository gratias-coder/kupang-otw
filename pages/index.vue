<template>
  <div>
    <!-- <NavTwo /> -->
    <section class="slider-one">
    <div class="slider-one__carousel">
      <swiper :options="swiperOptions">
      <swiper-slide>
      <div class="item slider-one__slider-1" style="background-image: url(/images/home2-slidebg-2.jpg);">
        <div class="container slider__content" style="text-align: center">
          <a class="mediabox video-play-btn" href="https://www.youtube.com/watch?v=dFBKl1pYn0w" title="Play Video" style="transition: none 0s ease 0s; text-align: inherit; line-height: 134px; border-width: 0px; margin: 0px; padding: 0px; letter-spacing: 0px; font-weight: 400; font-size: 30px;">
              <span class="fontello icon-play" style="color: #ff7e00; text-align: inherit; line-height: 134px; border-width: 0px; margin: 0px; padding: 0px; letter-spacing: 0px; font-weight: 400; font-size: 30px;"></span>
          </a>
          <div class="slider-one__title tp-caption tp-resizeme">we provide solution to<br> grow businesses</div>
          <a href="#" class="get-btn" style=""><span>get started</span></a>
          <!-- /.slider-one__text -->
        </div>
        <!-- /.container -->
      </div>
      <!-- /.item -->
      </swiper-slide>
      </swiper>
    </div>
  </section>
     <!-- <SliderTwo /> -->

   
     <!-- <ClientsLogo />  carousel-->


    <!-- <OfferTwo /> -->
    <section v-observe-visibility="onVisibilityChange" class="offer-area responsive-content inspire-area area-padding">
      <div class="offer-fluid">
          <div class="container">
              <div class="row offer-content">
                  <div class="inspire-list-box">
                      <div class="inspire-img mb-30px"></div><!-- end inspire-img -->
                      <div class="story-content">
                          <div class="top-story">
                              <span class="fontello icon-achievement success__icon"></span>
                              <span class="story__numbr counter">
                                <countTo :startVal='0' :endVal='startCounter ? 98903 : 0' :duration='3000'></countTo>
                              </span>
                              <span class="story__numbr">+</span>
                          </div><!-- end top-story -->
                          <p class="success__desc">client success stories by the help of avivon</p>
                      </div><!-- end story-content -->
                  </div><!-- end col-md-6 -->
                  <div class="offer-list-box">
                      <div class="offer-list">
                          <div class="avivon-heading">
                              <h2 class="avivon__title inspire-title">
                                  we inspire and help <br>
                                  our customers</h2>
                              <p class="avivon__desc mt-45px mb-40px">
                                  we inspire and help our customers expand their markets there are many
                                  variations of passages of lorem ipsum is simply free text available but
                                  majority have suffered alteration in some area that is not form by injected humour or
                                  randomised words don’t know which don't look even slightly believable.
                              </p>
                              <a href="#" class="get__btn">get started
                                  <span class="fontello icon-angle-double-right"></span>
                              </a>
                          </div><!-- end avivon-heading -->
                      </div><!-- end offer-list -->
                  </div><!-- end offer-list-box -->
              </div><!-- end row -->
          </div><!-- container-fluid -->
      </div><!-- end offer-fluid -->
  </section>

    <!-- <CasesCarousel /> -->
    
    <!-- <Testimonial /> -->
    <!-- <FunFact /> -->
    <!-- <ThinkArea /> -->
    <Blog />
    <!-- <Meet /> -->
    <Footer /> 
  </div>
</template>

<script>
import { Swiper, SwiperSlide, directive } from 'vue-awesome-swiper'
  import 'swiper/css/swiper.css'
   import countTo from 'vue-count-to';
  import { ObserveVisibility } from 'vue-observe-visibility'

  import Footer from "../components/Footer";
  // // import NavTwo from "../components/NavTwo";
  // // import SliderTwo from "../components/SliderTwo";
  // import ClientsLogo from "../components/ClientsLogo";
  // import OfferTwo from "../components/OfferTwo";
  // import CasesCarousel from "../components/CasesCarousel";
  // import Testimonial from "../components/Testimonial";
  // import FunFact from "../components/FunFact";
  // import ThinkArea from "../components/ThinkArea";
  import Blog from "../components/Blog";
  // import Meet from "../components/Meet";
  
  export default {
     components: {
        Swiper,
        SwiperSlide,
        countTo,
        Footer,
        Blog
      },
      
      directives: {
        swiper: directive,
         ObserveVisibility
      },
      data() {
        return {
          swiperOptions: {
            slidesPerView : 1,
            loop: false,
            speed: 1000,
            spaceBetween : 30,
            autoplay: {
                delay: 3000,
                disableOnInteraction: false
            },
             pagination: {
              el: '.swiper-pagination',
              type: 'bullets',
              clickable: true
            },
          }
        }
      },
      mounted() {
        MediaBox('.mediabox');
      },
       methods: {
        onVisibilityChange (isVisible) {
          if (isVisible){
            this.startCounter = true;
          }

        },
      }
  }
</script>

<style>
</style>

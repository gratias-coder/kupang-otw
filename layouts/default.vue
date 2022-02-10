<template>
<section>
   <div>
      <div :class="`body-overlay ${mobileToggle ? 'active' : ''}`"></div>
      <div :class="`offcanvas-menu ${mobileToggle ? 'active' : ''}`" class="offcanvas-menu">
          <div @click="mobileToggle = !mobileToggle" class="menu__close"></div><!-- end menu__close -->
          <ul class="off__menu">
              <li class="menu__title-only">home<a href="/index2">home 02</a></li>
              <!-- <li><a href="/">home 01</a></li>
              <li><a href="/index2">home 02</a></li>
              <li><a href="/index3">home 03</a></li> -->
              <li class="menu__title-only">pengumuman <i class="fas fa-angle-down"></i></li>
              <li><a href="/service1">pengumuman mingguan</a></li>
              <li><a href="/service2">kolekte</a></li>
              <!-- <li><a href="/single-service">single service</a></li> -->
              <li class="menu__title-only">profil <i class="fas fa-angle-down"></i></li>
              <!-- <li><a href="/about-us1">tentang gereja</a></li>
              <li><a href="/about-us2">tentang sistem</a></li> -->
              <!-- <li><a href="/our-mission">our mission</a></li> -->
              <li><a href="/our-history">sejarah</a></li>
              <!-- <li><a href="/our-partnership">partnership</a></li> -->
              <li class="menu__title-only">jadwal misa <i class="fas fa-angle-down"></i></li>
              <li><a href="/cases1">cases 01</a></li>
              <li><a href="/cases2">cases 02</a></li>
              <li><a href="/single-cases">single case</a></li>
              <li class="menu__title-only">artikel <i class="fas fa-angle-down"></i></li>
              <li><a href="/artikel">artikel</a></li>
              <!-- <li><a href="/single-blog">single blog</a></li> -->
              <li class="menu__title-only">contact <i class="fas fa-angle-down"></i></li>
              <li><a href="/contact">contact us</a></li>
          </ul>
      </div>
      <section :class="`menu-area menu--area ${sticky ? 'active' : ''}`">
          <div class="top-menu-area">
              <div class="container">
                  <div class="row">
                      <div class="col-md-12">
                        <div class="menu-full-width">
                            <div :class="`logo-box ${sticky ? 'active' : ''}`">
                                <div @click="mobileToggle = !mobileToggle" class="site-open">
                                    <span class="open__only"></span>
                                    <span class="open__only"></span>
                                    <span class="open__only"></span>
                                </div><!-- end site-open -->
                                <div class="logo">
                                    <nuxt-link to="/" title="Avivon">
                                    <!-- <img src="/images/logo-gereja-kpg.jpg" alt="logo" class="image-logo"> -->
                                   Gereja Kupang
                                    </nuxt-link>
                                </div><!-- end logo -->
                            </div><!-- end logo-box -->
                            <div class="main-menu">
                                <nav class="menu__wrapper">
                                    <ul class="dropdown-main">
                                        <li>
                                            <a href="/">home</a>
                                            
                                        </li>
                                        <li>
                                            <a href="/pengumuman">pengumuman</a>
                                        </li>
                                        <li> <a href="/kolekte">kolekte</a></li>
                                        <li>
                                            <!-- <a href="#">profil</a> -->
                                            <nuxt-link to="/profil">profil</nuxt-link>
                                            <!-- <div class="main__dropdown-menu"> -->
                                                <!-- <ul> -->
                                                  <!-- <li><nuxt-link to="/about-us1">tentang gereja</nuxt-link></li>
                                                  <li><nuxt-link to="/about-us2">tentang sistem</nuxt-link></li> -->
                                                  <!-- <li><nuxt-link to="/our-mission">our mission</nuxt-link></li> -->
                                                  <!-- <li><nuxt-link to="/our-history">sejarah</nuxt-link></li>
                                                  <li><nuxt-link to="/our-partnership">partnership</nuxt-link></li> -->
                                                <!-- </ul> -->
                                            <!-- </div> --> <!-- end main__dropdown-menu -->
                                        </li>
                                        <li>
                                            <a href="#">jadwal misa</a>
                                            <div class="main__dropdown-menu">
                                                <ul>
                                                  <li><nuxt-link to="/cases1">cases 01</nuxt-link></li>
                                                  <li><nuxt-link to="/cases2">cases 02</nuxt-link></li>
                                                  <li><nuxt-link to="/single-cases">single case</nuxt-link></li>
                                                </ul>
                                            </div><!-- end main__dropdown-menu -->
                                        </li>
                                        <li>
                                            <nuxt-link to="/artikel">artikel</nuxt-link>
                                            <!-- <a href="#">artikel</a>
                                            <div class="main__dropdown-menu">
                                                <ul>
                                                  <li><nuxt-link to="/artikel">artikel</nuxt-link></li>
                                                  <li><nuxt-link to="/single-blog">single blog</nuxt-link></li> -->
                                                <!-- </ul> -->
                                            <!--  </div> --> <!-- end main__dropdown-menu --> 
                                        </li> 
                                        <li>
                                            <nuxt-link to="/umat">umat</nuxt-link>
                                        </li>
                                    </ul>
                                </nav><!-- end menu__wrapper -->
                            </div><!-- end main-menu -->
                        </div><!-- end menu-full-width -->
                      </div><!-- end col-log-12 -->
                  </div><!-- end row -->
              </div><!-- end container -->
          </div><!-- end top-menu-area -->
      </section>
    </div>
  <div>
    <nuxt />
  </div>

 
</section>

  
</template>

<script>
  export default {
    components: {
    },
    data(){
        return {
          sticky: false,
          mobileToggle: false
        }
      },
    head(){
      return {
        title: "Sistem Informasi Gereja St. Petrus Kupang"
      }
    },
    mounted () {
      this.$nextTick(() => {
        this.$nuxt.$loading.start()
        setTimeout(() => this.$nuxt.$loading.finish(), 500)
      })
      window.addEventListener('scroll', this.handleScroll);
    },
     methods: {

        handleScroll () {
          if (window.scrollY > 70) {
            this.sticky = true
          }
          else if (window.scrollY < 70) {
            this.sticky = false
          }
        },

      }
  }
</script>

<style>
</style>

<template>
  <div>
    <section class="trusted-area breadcrumb-area text-center">
      <div class="trusted-fluid">
        <div class="container">
          <div class="row">
            <div class="col-md-12">
              <div class="trusted-content">
                <div class="trusted__title">
                  <ul class="bread__rumb-item">
                    <li class="active-item">
                      <nuxt-link to="/">home</nuxt-link>
                    </li>
                  </ul>
                  <h2 class="trusted__title-title">Artikel</h2>
                </div>
                <!-- end trusted__title -->
              </div>
              <!-- end trusted-content -->
            </div>
            <!-- end col-md-12 -->
          </div>
          <!-- end row -->
        </div>
        <!-- container -->
      </div>
      <!-- end trusted-fluid -->
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
       
        <!-- end col-md-12 -->
<section class="blog-area responsive-content area-padding">
        <div class="blog-fluid">
          <div class="container">
            <div class="row service-box blog-box text-left">
              <Blog
                v-for="(item, i) in dataArtikel"
                :key="i"
                :item="item"
                xs="12"
                sm="12"
                md="6"
                lg="4"
              />
            </div>
          </div>
        </div>
        
    </section>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
import Footer from "../../components/Footer.vue";
import Blog from "../../components/Blog";

export default {
  components: {
    Footer,
    Blog,
  },
  data: () => ({
    dataArtikel: [
      {
        title: "Artikel 1",
        publishDate: "11 Feb",
        excerpt: "Ini artikel 1",
        imageLink: "images/blog1.jpg",
      },

      {
        title: "Artikel 2",
        publishDate: "11 Feb",
        excerpt: "Ini artikel 1",
        imageLink: "images/blog1.jpg"
      },

      {
        title: "Artikel 3",
        publishDate: "11 Feb",
        excerpt: "Ini artikel 1",
        imageLink: "images/blog1.jpg"
      },

      
    ],
  }),
};
</script>

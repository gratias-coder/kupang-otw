<template>
  <section class="blog-area responsive-content area-padding">
      <div class="blog-fluid">
          <div class="container">
              <div class="row">
                  <div class="col-md-12 primary-padding-2 text-center">
                      <div class="avivon-heading">
                          <h2 class="avivon__title">Artikel</h2>
                      </div><!-- end avivon-heading -->
                  </div><!-- end col-md-12 -->
              </div><!-- end row -->
              <div class="row service-box blog-box text-left">
                  <div class="col-md-4 col-sm-6 col-xs-12">
                      <div class="shared-service">
                          <div class="shared__img">
                              <img src="/images/blog1.jpg" alt="blog image">
                              <div class="shared__date-item">
                                  <span> {{ $moment(item.publishDate).locale('id').format('DD MMMM YYYY') }}</span>
                                  <!-- <span>jul</span> -->
                              </div>
                          </div><!-- end shared-__img -->
                          <div class="shared-content">
                              <div class="service__title mb-30px">
                                  <h3 class="service__title-title">
                                      <a href="/single-blog">
                                          {{ item.author }}</a>
                                  </h3>
                              </div><!-- end service__title -->
                              <div class="service__desc mb-35px">
                                  <p class="service__desc-desc">
                                        {{ item.excerpt }}
                                  </p>
                              </div><!-- end service__desc -->
                              <div class="service__more">
                                  <a href="/single-blog" class="service__more-btn">
                                      read more <span class="fontello icon-angle-double-right"></span>
                                  </a>
                              </div><!-- end service__desc -->
                          </div><!-- end shared-content -->
                      </div><!-- end shared-service -->
                  </div><!-- end col-md-4 -->
                 
              </div><!-- end row -->
          </div><!-- container -->
      </div><!-- end blog-fluid -->
  </section>
</template>

<script>
    export default {
        name: "Artikel"
    }
</script>

<style scoped>

</style>

<template>
  <section class="blog-area responsive-content area-padding">
    <div class="blog-fluid">
      <div class="container">
        <div class="row service-box blog-box text-left">
          <div class="col-md-4 col-sm-6 col-xs-12">
            <div class="shared-service">
              <div class="shared__img">
                <!-- <img :src=item.imageLink alt="blog image" /> -->
                <div class="shared__date-item">
                  <span>
                    <!-- {{
                      $moment(item.publishDate)
                        .locale("id")
                        .format("DD MMMM YYYY")
                    }} -->
                   {{item.publishDate}} </span
                  >
                  <!-- <span>jul</span> -->
                </div>
              </div>
              <!-- end shared-__img -->
              <div class="shared-content">
                <div class="service__title mb-30px">
                  <h3 class="service__title-title">
                    <a href="/single-blog"> {{ item.title }}</a>
                  </h3>
                </div>
                <!-- end service__title -->
                <div class="service__desc mb-35px">
                  <p class="service__desc-desc">
                    {{ item.excerpt }}
                  </p>
                </div>
                <!-- end service__desc -->
                <div class="service__more">
                  <a href="/single-blog" class="service__more-btn">
                    Lebih lanjut
                    <span class="fontello icon-angle-double-right"></span>
                  </a>
                </div>
                <!-- end service__desc -->
              </div>
              <!-- end shared-content -->
            </div>
            <!-- end shared-service -->
          </div>
          <!-- end col-md-4 -->
        </div>
        <!-- end row -->
      </div>
      <!-- container -->
    </div>
    <!-- end blog-fluid -->
  </section>
</template>

<script>
export default {
    props: {
        item: {
            type: Object,
            default(){
                return {}
            }
        }
    }

};
</script>

<style scoped>
</style>

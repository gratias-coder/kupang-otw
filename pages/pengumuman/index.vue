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
                    <li>{{ title }}</li>
                  </ul>
                  <h2 class="trusted__title-title">Pengumuman</h2>
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
        <div class="container">
          <div class="row mb-30px masonary-layout">
            <div class="masonary-item">
              <div class="case-list">
                <div class="office-list-item"
                 v-for="(item, i) in dataPengumuman"
                    :key="i"
                    :item="item">
                  <div
                    class="office__name"
                   
                  >
                    <span class="office__desc-top">{{ item.author }}</span>
                    <h3 class="office__name-title">
                      <span>{{
                        item.pengumuman
                      }}</span>
                    </h3>
                    
                  </div>
                  <!-- end office__name -->
                  <br>
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
  </div>
</template>

<script>

export default ({
     data : () => ({
      dataPengumuman: [
          {
            author: "Admin",
            pengumuman: "Isi Pengumuman 1"
          },
          {
            author: "Admin",
            pengumuman: "Isi Pengumuman 2"
          },
          {
            author: "Admin",
            pengumuman: "Isi Pengumuman 3"
          }
        ]
     })
})
</script>

<template>
  <div>
    <section
      class="trusted-area breadcrumb-area text-center"
      style="background-image: url(/images/lingkungan.jpg)"
    >
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
                  <h2 class="trusted__title-title">Data Lingkungan</h2>
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
            <div class="case-list">
              
                  <v-col
                    v-for="(item, i) in dataList"
                    :key="i"
                    xs="12"
                    sm="12"
                    md="6"
                    lg="4"
                    class="masonary-item"
                  ><div class="office-list-item">
                <div class="office__name">
                    <span class="office__name-title">{{ item.title }}</span>
                    <!-- <div class="mt-4">
                      <li>{{ item.ling1 }}</li>
                      <li>{{ item.ling2 }}</li>
                      <li>{{ item.ling3 }}</li>
                    </div> -->

                     </div>
                
                <br />
              </div>
                  </v-col>
               
              
            </div>
            <!-- end col -->
          </div>
          <!-- end row -->
        </div>
        <!-- container -->
      </div>
      <!-- end ofc-caoursel-fluid -->
    </section>
    <Footer />
  </div>
</template>

<script>
import Footer from "../../components/Footer.vue";

export default {
  components: {
    Footer,
  },
  data: () => ({
    dataList: [
      {
        title: "KUB Stu. YAKOBUS RASUL",

        // ling1: "Maria",
        // ling2: "Elisabeth",
        // ling3: "Agnes",
      },
      {
        title: "KUB Sta. MARIA ROSA MISTIKA",

        // ling1: "Maria",
        // ling2: "Elisabeth",
        // ling3: "Agnes",
      },
      {
        title: "KUB Sta. MARIA RATU DAMAI",

        // ling1: "Maria",
        // ling2: "Elisabeth",
        // ling3: "Agnes",
      },
      {
        title: " KUB Stu. FRASISKUS DARI ASISI",
      },
      {
        title: "KUB Stu. YOHANES PAULUS II",
      },
      {
        title: "KUB Sta. LUSIA SUNGKAEN",
      },
      {
        title: "KUB Sta. FAMILIA",
      },
      {
        title: "KUB Stu. ANDREAS RASUL",
      },
      {
        title: "KUB Stu. YOSEPH",
      },
      {
        title: "KUB Sta. MARIA BERTABURAN RAHMAT PETUK",
      },
      {
        title: "KUB Sta. YOHANES MARIA VIANEY",
      },
      {
        title: "BIARA SUSTERAN BPS ( BUNDA PENGHARAPAN SELALU) NAIMATA ",
      },
      {
        title: "BIARA BRUDER CSA ( CONGREGASI Stu. ALOYSIUS) NAIMATA",
      },
    ],
  }),
};
</script>

<template>
    <div>
        <section class="trusted-area breadcrumb-area text-center"
        style="background-image: url(/images/profil.jpg)">
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
                                    <h2 class="trusted__title-title">Profil</h2>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
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
                            <div class="inspire-img mb-30px"
                            style="background-image: url(/images/santo_fransiskus.jpg)"></div>
                        </div>
                        <div class="offer-list-box">
                            <div class="offer-list">
                                <div class="avivon-heading">
                                    <h2 class="avivon__title inspire_title">
                                        Gereja Stasi Santo Fransiskus Xaverius Naimata, Kupang, NTT
                                    </h2>
                                    <p class="avivon__desc mt-45px mb-40px">
                                        Wilayah Stasi Santo Fransiskus Xaverius Naimata meliputi Kelurahan Naimata, 
                                        Kecamatan Maulafa, Kota Kupang, Provinsi Nusa Tenggara Timur, Kelurahan Liliba dan Binilaka. 
                                        Stasi ini bernaung di bawah Paroki St. Yosef Pekerja Penfui, Keuskupan Agung Kupang (KAK). 
                                        Stasi ini memiliki tiga kapela, yaitu kapela Naimata sebagai pusat stasi, kapela St. Tobias Sungkaen 
                                        dan Kapela Binilaka. Cikal-bakal stasi ini pada tahun 1948, dimulai oleh Pater Kriste, SVD 
                                        bersama Hendrikus Nggala dan Markus Seran.
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- <section class="offer-area responsive-content inspire-area area-padding"> -->
        <!-- <section 
          class="ofc-caoursel-area
                 responsive-content
                 recent-area
                 cases-area
                 area-padding
                 case-page-2">    
            <div class="ofc-caoursel-fuid">
                <div class="avivon-heading mb-30px" style="text-align: center">
                    <h2 class="avivon__title"> Sejarah</h2>
                </div>
            </div>
        </section> -->

        <!-- <section class="choose-area area-padding text-center">
            <div class="choose-fluid">
                <div class="container">
                    <div class="row choose-content responsive-content">
                        <div class="avivon-heading mb-30px" style="text-align: center">
                            <h2 class="avivon__title">
                                Sejarah
                            </h2>
                        </div>
                    </div>
                </div>
            </div>
        </section> -->
        <section class="choose-area area-padding text-center">
            <div>
            </div>
        </section>
        <TimelineSejarah />
        <SlideshowRomo />
        <Footer />
    </div>
</template>

<script>
import Footer from "../../components/Footer.vue";
import TimelineSejarah from "../../components/TimelineSejarah";
import SlideshowRomo from "../../components/SlideshowRomo";

export default ({
    components: {
        Footer,
        TimelineSejarah,
        SlideshowRomo,
    }
})
</script>

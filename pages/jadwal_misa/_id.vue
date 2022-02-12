<template>
    <div>

        <section class="trusted-area breadcrumb-area text-center"
            style="background-image: url(/images/thumbnail-jadwal.jpg)">
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
                                    <h2 class="trusted__title-title">Jadwal Misa</h2>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
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
                                v-for="(item, i) in dataJadwal"
                                    :key="i"
                                    :item="item">
                                    <div class="office__name"
                                    
                                    >
                                        <span class="office__desc-top">{{item.misa}}</span>
                                        <h3 class="office__name-title">
                                            <span>{{
                                                item.jadwal
                                                }}
                                            </span>
                                        </h3>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <Footer />
    </div>
</template>

<script>
import Footer from "../../components/Footer.vue";

export default ({
    components: {
        Footer,
    },
    data : () => ({
        dataJadwal: [
            {
                misa: "Misa Biasa",
                jadwal: "Minggu, pukul 08:00 WITA"
            },
            {
                misa: "Misa Lansia",
                jadwal: "Sabtu, pukul 17:00 WITA"
            }
        ]
    })
})
</script>

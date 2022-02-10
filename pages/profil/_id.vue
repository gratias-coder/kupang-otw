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
                            <div class="inspire-img mb-30px"></div>
                        </div>
                        <div class="offer-list-box">
                            <div class="offer-list">
                                <div class="avivon-heading">
                                    <h2 class="avivon__title inspire_title">
                                        Gereja Santo Petrus Kupang, NTT</h2>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </div>
</template>
<template>
    <div>
        <div class="position-relative pb-5">
            <img src="@/assets/images/jpg/large.jpg" class="position-absolute" style="width: 100%; height: 100%; object-fit: cover; z-index: -1;" alt="">
            <b-navbar toggleable="lg" type="dark" variant="light" class="px-3 py-2 text-center align-items-center">     
                <div class="d-flex justify-content-between w-100">
                    <b-navbar-nav class="text-center h-100">
                        <nuxt-link to="/" class="mr-3 p-2 text-dark text-decoration-none">Квартиры</nuxt-link>
                        <nuxt-link to="/" class="mr-3 p-2 text-dark text-decoration-none">Планировки</nuxt-link>
                        <nuxt-link to="/" class="mr-3 p-2 text-dark text-decoration-none">Информация о компексе</nuxt-link>
                        <nuxt-link to="/" class="mr-3 p-2 text-dark text-decoration-none">Связаться с нами</nuxt-link>
                    </b-navbar-nav>
                    <div>
                        
                        <b-button variant="warning">Оставить заявку</b-button>
                    </div>
                </div>
            </b-navbar>
            <b-container style="margin: 250px auto;">
                <h6 class="text-white text-center">Жилой комплекс</h6>
                <h1 class="text-white text-center">Parisien</h1>
                <div class="text-center mt-4 mb-5">
                    <b-button variant="warning">Выбрать квартиру</b-button>
                </div>
            </b-container>
        </div>
        <div class="bg-warning py-5">
            <b-container>
                <div class="text-center text-uppercase"><h4 class="m-0 font-weight-bold">особенности жилого комплекса</h4></div>
                <div class="d-flex justify-content-center mt-5">
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">6.5</h1>
                        <span class="text-secondary ml-1"><small>гектара</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">4</h1>
                        <span class="text-secondary ml-1"><small>дома</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">8</h1>
                        <span class="text-secondary ml-1"><small>этажей</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">576</h1>
                        <span class="text-secondary ml-1"><small>квартир</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">до1000</h1>
                        <span class="text-secondary ml-1"><small>парковочных мест</small></span>
                    </div>
                </div>
            </b-container>
        </div>
        <div>
            <img src="@/assets/images/png/object1.png" class="w-100" style="height: 100%; max-height: 802px;" alt="">
        </div>
        <div class="bg-warning py-5">
            <b-container>
                <div class="text-center text-uppercase"><h4 class="m-0 font-weight-bold">особенности квартир</h4></div>
                <div class="d-flex justify-content-center mt-5">
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">27+</h1>
                        <span class="text-secondary ml-1"><small>Lorem ipsum dolor sit amet.</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">53-141</h1>
                        <span class="text-secondary ml-1"><small>Lorem ipsum dolor sit amet consectetur adipisicing.</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">300</h1>
                        <span class="text-secondary ml-1"><small>Lorem ipsum dolor sit amet consectetur adipisicing.</small></span>
                    </div>
                    <div class="d-flex mx-3">
                        <h1 class="m-0 text-nowrap">180</h1>
                        <span class="text-secondary ml-1"><small>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eligendi, atque!</small></span>
                    </div>
                </div>
            </b-container>
        </div>
        <b-container class="py-5">
            <b-row>
                <b-col cols="3" class="text-center my-4" v-for="i in 8" :key="i">
                    <div class="w-100"><img src="@/assets/images/png/icon.png" class="rounded-circle border border-dark" style="width: 80px;" alt=""></div>
                    <div class="text-uppercase mt-2"><small>гармония пейзажа</small></div>
                </b-col>
            </b-row>
        </b-container>
        <b-container class="bg-dark text-center p-2 my-4">
            <h1 class="text-white text-uppercase">Галерея</h1>
            <b-row>
                <b-col cols="4" class="py-3" v-for="i in 9" :key="i">
                    <img src="@/assets/images/png/gallery1.png" class="w-100" alt="">
                </b-col>
            </b-row>
        </b-container>
        <b-container class="my-4 p-3" style="background: #3f417c;">
            <div class="mb-5">
                <h2 class="m-0 text-uppercase text-white">контакты</h2>
                <h3 class="text-uppercase text-white font-weight-normal">уникальный комплекс - для уникальных людей</h3>
            </div>
            <div class="d-flex align-items-center pb-4">
                <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d95913.44056607499!2d69.23376702582306!3d41.30244525704403!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2s!4v1609333243458!5m2!1sru!2s" width="745" height="554" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                <div class="p-3 mx-auto">
                    <h2 class="text-center text-uppercase text-white mb-5">Мы на карте</h2>
                    <div class="d-flex">
                        <img src="@/assets/images/svg/message.svg" class="mr-2 mt-1" style="width: 15px; height: 15px;" alt="">
                        <div class="text-white" style="max-width: 250px;">
                            Ташкент, Алмазарский район, пересечение улиц МКАД и Шимолий Олмазар
                        </div>
                    </div>
                    <div class="d-flex mt-3">
                        <img src="@/assets/images/svg/message.svg" class="mr-2 mt-1" style="width: 15px; height: 15px;" alt="">
                        <div class="text-white" style="max-width: 250px;">
                            Телефон : <small>+998</small> 71 200 88 22
                        </div>
                    </div>
                    <div class="d-flex">
                        <img src="@/assets/images/svg/message.svg" class="mr-2 mt-1" style="width: 15px; height: 15px;" alt="">
                        <div class="text-white" style="max-width: 250px;">
                            Email: info@mbc.uz
                        </div>
                    </div>
                    <div class="text-center mt-5">
                        <b-button variant="outline-light" pill><div class="text-uppercase p-2">Свяжитесь с нами</div></b-button>
                    </div>
                </div>
            </div>
        </b-container>
        <Footer />
    </div>
</template>

<script>
import Footer from '@/components/footer'

  export default {
  }
</script>
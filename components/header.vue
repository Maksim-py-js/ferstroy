<template>
    <div>
        <VueSlickCarousel v-bind="mainSlider" class="p-0 m-0 border-0 position-absolute" style="height: 940px !important;">
            <div class="main-slide-image">
                <img src="@/assets/images/png/slide_1.png" alt="">
                <div class="hover-block-top"></div>
                <div class="hover-block-main"></div>
            </div>
            <div class="main-slide-image">
                <img src="@/assets/images/png/slide_2.png" alt="">
                <div class="hover-block-top"></div>
                <div class="hover-block-main"></div>
            </div>
            <div class="main-slide-image">
                <img src="@/assets/images/png/slide_3.png" alt="">
                <div class="hover-block-top"></div>
                <div class="hover-block-main"></div>
            </div>
            <div class="main-slide-image">
                <img src="@/assets/images/png/slide_4.png" alt="">
                <div class="hover-block-top"></div>
                <div class="hover-block-main"></div>
            </div>
        </VueSlickCarousel>
        
            
           

        <div  style="height: 940px;">


            <div class="container_1290 position-relative">
                <b-navbar toggleable="lg" variant="transparent" class="p-0 text-center align-items-center">
                    <div class="d-flex justify-content-between align-items-center w-100" style="margin-top: 20px;">
                        <div class="header__logo">
                            <div class="header__logo_image">
                                <div class="header__logo_text">logo</div>
                                <!-- <img src="@/assets/images/png/slide_3.png"> -->
                            </div>
                            <div class="header__logo_name">Название компании</div>
                        </div>
                        <b-navbar-nav class="text-center align-items-center h-100">
                            <nuxt-link to="/" class="nav_item text-decoration-none">О компании</nuxt-link>
                            <nuxt-link to="/object_page" class="nav_item text-decoration-none">Объекты</nuxt-link>
                            <nuxt-link to="/" class="nav_item text-decoration-none">Уникальность проектов</nuxt-link>
                            <nuxt-link to="/" class="nav_item text-decoration-none">Карьера</nuxt-link>
                            <nuxt-link to="/" class="nav_item text-decoration-none">Тендеры</nuxt-link>
                            <nuxt-link to="/" class="nav_item text-decoration-none">Контакты</nuxt-link>

                            <!-- <nuxt-link to="/map" class="nav_item text-decoration-none">Карта</nuxt-link>
                            <nuxt-link to="/super_admin/statistic" class="nav_item text-decoration-none">Администратор</nuxt-link>
                            <nuxt-link to="/parlament/statistic" class="nav_item text-decoration-none">Хокимиат</nuxt-link> -->
                            <div class="position-relative" style="height: 26px; width: 61px;">
                                <div class="language-block position-absolute">
                                    <b-button variant="transparent" class="language-btn shadow-none">
                                        Рус
                                    </b-button>
                                    <b-button variant="transparent" class="language-btn shadow-none">
                                        Eng
                                    </b-button>
                                    <b-button variant="transparent" class="language-btn shadow-none">
                                        Узб
                                    </b-button>
                                </div>
                            </div>
                        </b-navbar-nav>
                        <div>
                            <div><a href="tel:+712008822" class="header__phone text-decoration-none">(71) 200 88 22</a></div>
                            <div><a href="tel:+712008822" class="header__phone_text">Связаться с нами</a></div>                            
                        </div>
                    </div>
                </b-navbar>    
                <div class="selectProperty" style="margin-top: 220px; text-align: center;">
                    <b-button @click="openSearchBar(SearcBarState)" variant="transparent" class="search-dropdown shadow-none">Подобрать недвижимость</b-button>             
                </div>                
                <div class="selectProperty__name">Резеденция вашей мечты</div>            
            </div>

            <div v-bind:class="{ open_container: SearcBarState }" class="close_container bg-white">                            
                <div class="container_1290" style="padding: 20px 0;">
                    <div class="d-flex justify-content-between align-items-center">
                        <div class="m-0 h-100 search__title">Поиск новостроек</div>
                        <b-button 
                            variant="transparent" 
                            @click="closeSearchBar(SearcBarState)"
                            class="close-search align-items-center p-0 m-0 shadow-none d-flex algn-items-center"
                        >
                            <span>Скрыть поиск</span>
                            <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg" style="margin-left: 18px;">
                                <path d="M16.772 0L19.9809 3.21199L3.20893 20L0 16.788L16.772 0Z"/>
                                <path d="M3.22801 0L0.0190783 3.21199L16.7911 20L20 16.788L3.22801 0Z"/>
                            </svg>   
                        </b-button>
                    </div>
                </div>
                <div class="container_1290" style="padding: 10px 0 0 0;">
                    <div>                        
                        <input type="text" placeholder="Название новостройки или застройщика" class="search__input"></input>
                    </div>
                    <div class="d-flex flex-wrap justify-content-between">
                        <div>
                            <div class="search__title_sm">Расположение</div>
                            <div class="d-flex mt-4">
                                <v-selectize 
                                    placeholder="Город"
                                    v-model="selected_locationOptions.country" 
                                    :options="locationOptions.countries"
                                    class="select-300"
                                />
                                <v-selectize 
                                    placeholder="Район"
                                    v-model="selected_locationOptions.district" 
                                    :options="locationOptions.districts"
                                    class="select-200"
                                />
                                <v-selectize 
                                    placeholder="Улица"
                                    v-model="selected_locationOptions.street" 
                                    :options="locationOptions.streets"
                                    class="select-200"
                                />
                            </div>
                        </div>
                         <div>
                            <div class="search__title_sm">Цена за квартиру</div>
                                <div class="d-flex mt-4">          
                                    <b-form class="d-flex">
                                        <input
                                            id="input-1"
                                            type="number"
                                            placeholder="от"
                                            class="search__input shadow-none"
                                            style="width: 250px; margin-right: 20px;"
                                        ></input>
                                        <input
                                            id="input-1"
                                            type="number"
                                            placeholder="до"
                                            class="search__input shadow-none"
                                            style="width: 250px;"
                                        ></input>
                                    </b-form>
                                </div>
                            </div>
                    </div>
                    <div class="d-flex flex-wrap">
                        <div>
                            <div class="search__title_sm">Комнатность</div>
                            <div class="d-flex custom-radio-label mt-4">
                                <div class="text-roomines">Студии</div>
                                <div style="margin-right: 20px;" v-for="item in roominessItems" :key="item.id">
                                    <input 
                                        type="radio" 
                                        class="custom-radio-number" 
                                        :class="item.classDisabled"
                                        v-model="selected_roominess" 
                                        :value="item.size" 
                                        :id="item.id" 
                                        :name="item.id"
                                        :disabled="item.disabled"
                                    ></input>
                                    <label :for="item.id" class="custom-radio-number-label"><span>{{ item.size }}</span></label> 
                                </div>
                                <div class="text-roomines" style="padding: 19px 56px;">Пентхаус</div>
                            </div>  
                        </div>
                        <div>
                            <div class="search__title_sm">Срок сдачи</div>
                            <div class="d-flex mt-4">
                                <v-selectize 
                                    placeholder="Любой"
                                    v-model="selected_deadline.deadline" 
                                    :options="deadlineItems.deadlines"
                                    class="select-190"
                                />
                                <v-selectize 
                                    placeholder="Есть скидки"
                                    v-model="selected_deadline.discount" 
                                    :options="deadlineItems.discounts"
                                    class="select-190"
                                />
                            </div>
                        </div>
                    </div>

                    <div class="d-flex flex-wrap mt-5">
                        <b-button variant="transparent" class="sorting-btn shadow-none">С отделкой</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Ипотека</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Матерински капитал</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Эскроу-счет</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Старт продаж</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Панорамные окна</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Ипотека с первым взносом 0%</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Рассрочка</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Рядом парк</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Онлайн покупка</b-button>
                    <div>
                        <v-selectize 
                            placeholder="Кол-во квартир на этаже"
                            v-model="selected_apartmantPerFloor" 
                            :options="apartmantPerFloor"
                            class="select-300"
                        />
                    </div>
                    </div>
                    <b-button variant="transparent" class="btn-lessParams shadow-none mt-3 mb-3">Меньше параметров</b-button>
                    
                    <div class="d-flex flex-wrap mt-4">
                        <b-button variant="transparent" class="sorting-btn shadow-none">Посмотреть 146 ЖКХ</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none">Новостройки премиум-класса</b-button>
                        <b-button variant="transparent" class="sorting-btn shadow-none" to="/map">
                            <svg width="20" height="25" viewBox="0 0 20 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9.72222 0C4.36154 0 0 4.27148 0 9.52149C0 11.5991 0.670086 13.5732 1.93946 15.2295L9.12293 24.7046C9.14088 24.7276 9.1683 24.7364 9.18825 24.7569C9.54722 25.1334 10.0652 25.0386 10.321 24.7046C12.3896 22.0015 16.1813 16.9531 17.6391 15.0488C17.6391 15.0488 17.6396 15.0474 17.6401 15.0464L17.6491 15.0347C18.8237 13.4185 19.4444 11.5122 19.4444 9.52149C19.4444 4.27148 15.0829 0 9.72222 0ZM9.72222 14.6582C6.83597 14.6582 4.47721 12.3481 4.47721 9.52149C4.47721 6.69482 6.83597 4.38477 9.72222 4.38477C12.6085 4.38477 14.9672 6.69482 14.9672 9.52149C14.9672 12.3481 12.6085 14.6582 9.72222 14.6582Z"/>
                            </svg>
                            Поиск на карте
                        </b-button>
                    </div>

                </div>
            </div> 
                  
        </div>
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

import 'selectize/dist/css/selectize.css'
import VSelectize from '@isneezy/vue-selectize'

  export default {
    components: { VueSlickCarousel, VSelectize },
    methods: {
        openSearchBar(SearcBarState) {
            this.SearcBarState = true;
            console.log(SearcBarState);
        },       
        closeSearchBar(SearcBarState) {
            this.SearcBarState = false;
            console.log(SearcBarState);
        }
    },
    data() {
      return {
        SearcBarState: false,


        mainSlider: {
            arrows: false,
            dots: true,
            slidesToShow: 1,
            autoplay: true,
            autoplaySpeed: 3500,
            vertical: true
        },
        roominessItems: [
          {
            id: 'num-1',
            size: "1",
            value: '1'
          },
          {
            id: 'num-2',
            size: "2",
            value: '2'
          },
          {
            id: 'num-3',
            size: "3",
            value: '4'
          },
          {
            id: 'num-4',
            size: "4",
            value: '4'
          },
          {
            id: 'num-5',
            size: "5+",
            value: '5'
          }
        ],        
        selected_roominess: '', 
        deadlineItems: {
            deadlines: [
                '1 мес',
                '3 мес',
                '5+ мес'
            ],
            discounts: [
                'Да',
                'Нет'
            ]
        },   
        selected_deadline: {
            deadline: null,
            discount: null
        },

        locationOptions: {
            countries: [
                'Фергана',
                'Ташкент',
                'Самарканд'
            ],
            districts: [
                'Юнособадский',
                'Сергелийский',
                'Мирабадский'
            ],
            streets: [
                'Ислама Каримова',
                'Зухура Кобулова',
                'Лабзак'
            ]
        },
        selected_locationOptions: {
            country: null,
            district: null,
            street: null
        },
        apartmantPerFloor: [
          '1',
          '2',
          '3',
          '4',
          '5+'
        ],
        selected_apartmantPerFloor: null
      }
    }
  }
</script>
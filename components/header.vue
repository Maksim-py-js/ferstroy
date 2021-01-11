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
                            <nuxt-link to="/" class="header__nav_item text-decoration-none">О компании</nuxt-link>
                            <nuxt-link to="/object_page" class="header__nav_item text-decoration-none">Объекты</nuxt-link>
                            <nuxt-link to="/" class="header__nav_item text-decoration-none">Уникальность проектов</nuxt-link>
                            <nuxt-link to="/" class="header__nav_item text-decoration-none">Карьера</nuxt-link>
                            <nuxt-link to="/" class="header__nav_item text-decoration-none">Тендеры</nuxt-link>
                            <nuxt-link to="/" class="header__nav_item text-decoration-none">Контакты</nuxt-link>

                            <!-- <nuxt-link to="/map" class="header__nav_item text-decoration-none">Карта</nuxt-link>
                            <nuxt-link to="/super_admin/statistic" class="header__nav_item text-decoration-none">Администратор</nuxt-link>
                            <nuxt-link to="/parlament/statistic" class="header__nav_item text-decoration-none">Хокимиат</nuxt-link> -->
                            <b-nav-item-dropdown align="center" text="Рус" class="header__language">
                                <b-dropdown-item href="#">Англ</b-dropdown-item>
                                <b-dropdown-item href="#">Узб</b-dropdown-item>
                            </b-nav-item-dropdown>
                        </b-navbar-nav>
                        <div>
                            <div><a href="tel:+712008822" class="header__phone text-decoration-none">(71) 200 88 22</a></div>
                            <div><a href="tel:+712008822" class="header__phone_text text-decoration-none">Связаться с нами</a></div>                            
                        </div>
                    </div>
                </b-navbar>    
                <div class="selectProperty" style="margin-top: 220px; text-align: center;">
                    <b-button @click="openDropdown(isActive)" variant="transparent" class="search-dropdown shadow-none">Подобрать недвижимость</b-button>             
                </div>                
                <div class="selectProperty__name">Резеденция вашей мечты</div>            
            </div>

            <div v-bind:class="{ open_container: isActive }" class="close_container bg-white">                            
                <div class="container_1290" style="padding: 20px 0;">
                    <div class="d-flex justify-content-between align-items-center">
                        <h5 class="m-0 h-100">Поиск новостроек</h5>
                        <b-button variant="transparent" class="openMore-btn shadow-none">
                            <span>Раскрыть поиск</span>
                            <img src="@/assets/images/svg/arrow-down-yellow.svg" style="width: 14px; height: 9px; line-height: 0; margin: 0 0 3px 15px;">
                        </b-button>
                        <b-button 
                            variant="transparent" 
                            @click="closeDropdown(isActive)"
                            class="close-search align-items-center p-0 m-0 shadow-none d-flex algn-items-center"
                        >
                            <span>Скрыть поиск</span>
                            <img src="@/assets/images/svg/close.svg" style="margin-left: 18px; width: 20px; height: 20px;line-height: 0;">    
                        </b-button>
                    </div>
                </div>
            </div> 
                  
        </div>
        
        
        <!-- <div>
            <b-input-group class="mt-3">
                <template #append>
                    <b-button variant="outline-light" class="border-primary border-left-0"><img src="@/assets/images/svg/loupe.svg" style="width: 15px; height: 15px;" alt=""></b-button>
                </template>
                <b-form-input placeholder="Удобный поиск новостроек" class="bg-white border-primary border-right-0"></b-form-input>
            </b-input-group>
        </div>
        <div class="d-flex flex-wrap py-3 px-4">
            <div>
                <div class="text-secondary"><small>Расположение</small></div>
                <div class="d-flex mt-3">
                <b-form-select v-model="selected_locationOptions" :options="locationOptions"></b-form-select>
                <b-button variant="light" class="ml-3 mr-1">Метро</b-button>
                <b-button variant="light" class="mx-1">МЦД</b-button>
                <b-button variant="light" class="mx-1">Районы</b-button>
                </div>
            </div>
            <div class="ml-3">
                <div class="text-secondary"><small>До метро не более</small></div>
                <div class="d-flex mt-3">
                <b-form-input
                    id="input-1"
                    type="number"
                    placeholder="Минут"
                    required
                    class="mr-1"
                ></b-form-input>
                <b-form-select v-model="selected_timeOptions" :options="timeOptions"></b-form-select>
                </div>
            </div>
        </div>
        <div class="d-flex flex-wrap py-3 px-4">
            <div>
                <div class="text-secondary mb-3"><small>Цена за квартиру</small></div>
                <div class="d-flex">          
                    <b-form class="d-flex">
                        <b-form-group class="mr-1">
                        <b-form-input
                            id="input-1"
                            type="number"
                            placeholder="от"
                            required
                        ></b-form-input>
                        </b-form-group>
                        <b-form-group>
                        <b-form-input
                            id="input-1"
                            type="number"
                            placeholder="до"
                            required
                        ></b-form-input>
                        </b-form-group>
                    </b-form>
                </div>
            </div>
            <div class="ml-3">
                <div class="text-secondary mb-3"><small>Комнатность</small></div>
                <b-form-select v-model="selected_roominessOptions" :options="roominessOptions"></b-form-select>
            </div>
            <div class="ml-3">
                <div class="text-secondary mb-3"><small>Срок сдачи</small></div>
                <div class="d-flex">
                <b-form-select v-model="selected_deadlineOptions" :options="deadlineOptions" class="mr-3"></b-form-select>
                <b-button variant="light" style="white-space: nowrap;">Есть скидки</b-button>
                </div>
            </div>
        </div>
        <div class="d-flex flex-wrap py-3 px-4">
            <b-button variant="light" class="mr-1 mb-1">С отделкой</b-button>
            <b-button variant="light" class="mr-1 mb-1">Ипотека</b-button>
            <b-button variant="light" class="mr-1 mb-1">Матерински капитал</b-button>
            <b-button variant="light" class="mr-1 mb-1">Эскроу-счет</b-button>
            <b-button variant="light" class="mr-1 mb-1">Старт продаж</b-button>
            <b-button variant="light" class="mr-1 mb-1">Ипотека с первым взносом 0%</b-button>
            <b-button variant="light" class="mr-1 mb-1">Рассрочка</b-button>
            <b-button variant="light" class="mr-1 mb-1">Панорамные окна</b-button>
            <b-button variant="light" class="mr-1 mb-1">Рядом парк</b-button>
            <b-button variant="light" class="mr-1 mb-1">Онлайн покупка</b-button>
        <div>
            <b-form-select v-model="selected_apartmantPerFloor" :options="apartmantPerFloor" class="mr-1 mb-1"></b-form-select>
        </div>
        </div>
        <b-button variant="transparent" class="text-primary px-4"><small>Меньше параметров</small></b-button>
        <div class="d-flex px-4 py-3">
            <b-button class="mr-3" variant="warning">Посмотреть 146 ЖК</b-button>
            <b-button class="mr-3" variant="outline-primary">Новостройки премиум класса</b-button>
            <b-button class="mr-3" variant="primary">Поиск на карте</b-button>
        </div> -->
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

  export default {
    components: { VueSlickCarousel },
    methods: {
        openDropdown(isActive) {
            this.isActive = true;
            console.log(isActive);
        },
        closeDropdown(isActive) {
            this.isActive = false;
            console.log(isActive);
        }
    },
    data() {
      return {
        isActive: false,

        mainSlider: {
            arrows: false,
            dots: true,
            slidesToShow: 1,
            autoplay: true,
            autoplaySpeed: 3500,
            vertical: true
        },
        deadlineRangeValue: 'Сдана',
        selected_locationOptions: null,
        selected_timeOptions: null,
        selected_roominessOptions: null,
        selected_deadlineOptions: null,
        selected_apartmantPerFloor: null,
        locationOptions: [
          { value: null, text: 'Выберите город' },
          { value: '1', text: 'Город 1' },
          { value: '2', text: 'Город 2' },
          { value: '3', text: 'Город 3' },
        ],
        timeOptions: [
          { value: null, text: 'Выбрать' },
          { value: '1', text: '5' },
          { value: '2', text: '10' },
          { value: '3', text: '15' },
        ],
        roominessOptions: [
          { value: null, text: 'Выбрать' },
          { value: '1', text: '1' },
          { value: '2', text: '2' },
          { value: '3', text: '3' },
          { value: '4', text: '4' },
          { value: '5', text: '5+' },
        ],
        deadlineOptions: [
          { value: null, text: 'Выбрать' },
          { value: '1', text: '1 месяц' },
          { value: '2', text: '2 месяца' },
          { value: '3', text: '3 месяца' },
          { value: '4', text: '4 месяца' },
          { value: '5', text: '5+ месяцев' },
        ],
        apartmantPerFloor: [
          { value: null, text: 'Кол-во квартир на этаже' },
          { value: '1', text: '1' },
          { value: '2', text: '2' },
          { value: '3', text: '3' },
          { value: '4', text: '4' },
          { value: '5', text: '5+' },
        ],
      }
    }
  }
</script>
<template>
    <div>
        <div class="position-relative pb-5">
            <img src="@/assets/images/jpg/large.jpg" class="position-absolute" style="width: 100%; height: 100%; object-fit: cover; z-index: -1;" alt="">
            <b-navbar toggleable="lg" type="dark" variant="transparent" class="p-0 text-center align-items-center">
                
                <b-container>
                    <div class="d-flex justify-content-between w-100">
                    <b-navbar-nav class="text-center h-100">
                        <nuxt-link to="/" class="mr-3 p-2 text-white text-decoration-none">О компании</nuxt-link>
                        <nuxt-link to="/object_page" class="mr-3 p-2 text-white text-decoration-none">Объекты</nuxt-link>
                        <nuxt-link to="/map" class="mr-3 p-2 text-white text-decoration-none">Карта</nuxt-link>
                        <nuxt-link to="/super_admin/statistic" class="mr-3 p-2 text-white text-decoration-none">Администратор</nuxt-link>
                        <nuxt-link to="/parlament/statistic" class="mr-3 p-2 text-white text-decoration-none">Хокимиат</nuxt-link>
                        <b-nav-item-dropdown text="Рус">
                        <b-dropdown-item href="#">Англ</b-dropdown-item>
                        <b-dropdown-item href="#">Узб</b-dropdown-item>
                        </b-nav-item-dropdown>
                    </b-navbar-nav>
                    <div>
                        <a href="tell:+72712208822" class="text-white text-decoration-none"><h2>71 220 88 22</h2></a>
                        <b-button variant="outline-light" pill>Связаться с нами</b-button>
                    </div>
                    </div>
                </b-container>
            </b-navbar>
            <b-container style="margin-top: 200px;">
                <!-- <b-input-group class="mt-3">
                    <template #append>
                        <b-button variant="light"><img src="@/assets/images/svg/loupe.svg" style="width: 15px; height: 15px;" alt=""></b-button>
                    </template>
                    <b-form-input placeholder="Удобный поиск новостроек" class="bg-light border-0"></b-form-input>
                </b-input-group> -->
                <b-dropdown
                    class="search-dropdown"
                    text="Удобный поиск новостроек"                    
                    no-flip
                    variant="light"
                    menu-class="w-100"
                >
                    <b-container class="mb-5 pb-3">
                        <div class="bg-light py-3 px-4">
                        <div class="d-flex justify-content-between align-items-center">
                            <h5 class="m-0 h-100">Поиск новостроек</h5>
                        </div>
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
                        </div>
                    </b-container>
                </b-dropdown>


                <h1 class="text-white text-center mt-5" style="text-transform: uppercase;">nest one</h1>
                <h6 class="text-white text-center">Первый небоскреб Узбекистана</h6>
                <div class="text-center mt-4 mb-5">
                    <b-button variant="outline-light" pill>Узнать подробнее ></b-button>
                </div>
            </b-container>
        </div>
        
        
    </div>
</template>

<script>
  export default {
    data() {
      return {
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
<template>
    <div class="map-body">  
        
        <div class="position-relative">
            <no-ssr>
                <yandex-map 
                    :coords="coords" 
                    :zoom="14" 
                    style="height: 860px"
                >
                    <ymap-marker 
                        marker-id="123" 
                        :coords="markers[0]"
                        :icon="markerIcon"
                        :balloon-template="balloonTemplate"

                    />
                    <ymap-marker 
                        marker-id="124" 
                        :coords="markers[1]"
                        :icon="markerIcon"      
                        :balloon-template="balloonTemplate"
                    />
                </yandex-map>
            </no-ssr>
            <div class="position-absolute h-99 bg-white p-3" style="top: 50%; transform: translateY(-50%); right: 20px; width: 310px;">
                <div class="mb-2">
                    <div class="cityBtn">Фергана и Обл</div>
                </div>
                <div class="filter">
                    <div class="filterName mt-2 mb-1">Цена</div>
                    <div class="justify-content-between inputBox">
                        <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                            <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="от 0 млн сум"></b-form-input>
                            <div class="line">-</div>
                            <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="до 1 млрд сум"></b-form-input>
                        </b-input-group>
                    </div>
                    <no-ssr>
                        <div class="filter__rangeSlider">
                            <vue-range-slider v-model="value" dot-size=30 height=10></vue-range-slider>
                        </div>
                    </no-ssr>
                </div>
                <div class="filter">
                    <div class="filterName mt-2 mb-1">Срок сдачи</div>
                    <div class="justify-content-between inputBox">
                        <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                            <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="Сданы"></b-form-input>
                            <div class="line">-</div>
                            <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="По 2024"></b-form-input>
                        </b-input-group>
                    </div>
                </div>
                <div class="filter">
                    <b-form-group v-slot="{ ariaDescribedby }">
                        <b-form-radio-group
                            id="btn-radios-1"
                            v-model="selected"
                            :options="options"
                            :aria-describedby="ariaDescribedby"
                            name="radios-btn-default"
                            buttons
                        ></b-form-radio-group>
                    </b-form-group>
                </div>
                <div class="filter">
                    <div class="filterName mt-2 mb-1">Площадь</div>
                    <div class="justify-content-between inputBox">
                        <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                            <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="от 20"></b-form-input>
                            <div class="line">-</div>
                            <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="до 200"></b-form-input>
                        </b-input-group>
                    </div>
                </div>
                <div class="filter">
                    <div class="filterName mt-2 mb-1">Застройщики</div>
                    <v-selectize 
                        placeholder="Выберите застройщика"
                        v-model="selected_finishing" 
                        :options="finishing"
                        class="searchResult__leftRow_selectize select-260"
                        style="margin: 0;"
                    />
                </div>
                <div class="filter houseFilter">
                    <b-form-group v-slot="{ ariaDescribedby }">
                        <b-form-radio-group
                            id="btn-radios-2"
                            v-model="selected2"
                            :options="options2"
                            :aria-describedby="ariaDescribedby"
                            name="radios-btn-default"
                            buttons
                        ></b-form-radio-group>
                    </b-form-group>
                </div>
            </div>
        </div>
        <div class="container_1290">
            <b-breadcrumb :items="breadcrumbItems" variant="transparent" class="mt-5 mb-4"></b-breadcrumb>
            <h3 class="main__title">Карта Новостроек или как найти идеальное жильё в Фергане</h3>
            <b-row>
                <b-col>
                    <h6 class="discription__title">Квартиры в новостройках Ферганы</h6>
                    <span class="main__text">
                        пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                    </span>
                    <div class="map">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d95913.44056607499!2d69.23376702582306!3d41.30244525704403!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2s!4v1609333243458!5m2!1sru!2s" width="100%" height="400px" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                        <div class="position-absolute h-100 bg-white p-3 miniFilter">
                            <div class="mb-2">
                                <div class="cityBtn">Фергана и Обл</div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Цена</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="от 0 млн сум"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="до 1 млрд сум"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Срок сдачи</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="Сданы"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="По 2024"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                        </div>
                    </div>
                    <h6 class="discription__title">Квартиры в новостройках Ферганы</h6>
                    <span class="main__text">
                        пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                    </span>
                    <div class="map">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d95913.44056607499!2d69.23376702582306!3d41.30244525704403!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2s!4v1609333243458!5m2!1sru!2s" width="100%" height="400px" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                        <div class="position-absolute h-100 bg-white p-3 miniFilter">
                            <div class="mb-2">
                                <div class="cityBtn">Фергана и Обл</div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Цена</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="от 0 млн сум"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="до 1 млрд сум"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Срок сдачи</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="Сданы"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="По 2024"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                        </div>
                    </div>
                    <h6 class="discription__title">Квартиры в новостройках Ферганы</h6>
                    <span class="main__text">
                        пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                    </span>
                </b-col>
                <b-col>
                    <h6 class="discription__title">Квартиры в новостройках Ферганы</h6>
                    <span class="main__text">
                        пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                    </span>
                    <div class="map">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d95913.44056607499!2d69.23376702582306!3d41.30244525704403!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2s!4v1609333243458!5m2!1sru!2s" width="100%" height="400px" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                        <div class="position-absolute h-100 bg-white p-3 miniFilter">
                            <div class="mb-2">
                                <div class="cityBtn">Фергана и Обл</div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Цена</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="от 0 млн сум"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="до 1 млрд сум"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                            <div class="filter">
                                <div class="filterName mt-2 mb-1">Срок сдачи</div>
                                <div class="justify-content-between inputBox">
                                    <b-input-group class="d-flex shadow-none justify-content-between align-items-center">
                                        <b-form-input type="number" min="0" class="border-0 shadow-none" placeholder="Сданы"></b-form-input>
                                        <div class="line">-</div>
                                        <b-form-input type="number" min="0" class="border-0 shadow-none numInput" placeholder="По 2024"></b-form-input>
                                    </b-input-group>
                                </div>
                            </div>
                        </div>
                    </div>
                    <h6 class="discription__title">Квартиры в новостройках Ферганы</h6>
                    <span class="main__text">
                        пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                        <br/>
                        <br/>
                        Квартиры в новостройках Ферганы пользуются большим спросом, на нашем сайте можете размещать не ограниченное колличество квартир в любой из категорий. А так же размещать рекламные и информационные статьи. Удачи!
                    </span>
                </b-col>
            </b-row>
        </div>
    </div>
</template>

<script>
    import 'selectize/dist/css/selectize.css'
    import 'vue-range-component/dist/vue-range-slider.css'
    import VSelectize from '@isneezy/vue-selectize'
    import NoSSR from 'vue-no-ssr'

    let components = {
        /**
         * Add No Server Side Render component
         * to make client DOM math the server DOM
         */
        
        VSelectize,
        'no-ssr': NoSSR
    }
    if (process.browser) {
        // in older versions of nuxt, it's process.BROWSER_BUILD
        let VueRangeSlider = require('vue-range-component').default
        components['vue-range-slider'] = VueRangeSlider
    }

    export default { 
        layout: 'main',
        components,
        data() {
            return {
                breadcrumbItems: [
                    {
                        text: 'Главная',
                        href: '/'
                    },
                    {
                        text: 'Карта новостроек',
                        active: true
                    }
                ],
                map_deadlineRangeMinValue: 'Сдана',
                map_deadlineRangeMaxValue: '2024',
                map_deadlineRangeValue: 'Сдана',
                map_priceRangeValue: '200',
                map_selected_roominessOptions: null,
                map_selected_deadlineOptions: null,
                map_roominessOptions: [
                    { value: null, text: 'Выбрать' },
                    { value: '1', text: '1' },
                    { value: '2', text: '2' },
                    { value: '3', text: '3' },
                    { value: '4', text: '4' },
                    { value: '5', text: '5+' },
                ],
                map_deadlineOptions: [
                    { value: null, text: 'Выбрать' },
                    { value: '1', text: '1 месяц' },
                    { value: '2', text: '2 месяца' },
                    { value: '3', text: '3 месяца' },
                    { value: '4', text: '4 месяца' },
                    { value: '5', text: '5+ месяцев' },
                ],
                selected: 'radio1',
                options: [
                    { text: 'Студия', value: 'radio1' },
                    { text: '1', value: 'radio2' },
                    { text: '2', value: 'radio3' },
                    { text: '3', value: 'radio4' },
                    { text: '4', value: 'radio5' }
                ],
                selected2: 'radio21',
                options2: [
                    { text: 'Квартиры', value: 'radio21' },
                    { text: 'Апартаменты', value: 'radio22' },
                    { text: 'Таунхаусы', value: 'radio23' },
                ],
                finishing: [
                    'все',
                    'mirabad avenue',
                    'Golden House'
                ],
                selected_finishing: null,
                value: [0, 100],
                coords: [40.388404, 71.780839],
                markers: [
                    [40.381318, 71.804794],
                    [40.377401, 71.786434]          
                ],
                markerIcon: {
                    layout: 'default#imageWithContent',
                    imageHref: `${require('@/assets/images/svg/Vector.svg')}`,
                    imageSize: [89, 113],
                    imageOffset: [-40, -110],
                    content: '',
                    contentOffset: [7, 6],
                    contentLayout: '<div class="markImage"><img src="https://mirabad.uz/upload/kelnik.adminpage/c0c/c0cf81c2a22ec8ec0c77335fe14b9533.jpg"></div>'
                },
                showMap: false
            }
        },
        mounted() { this.showMap = true },
        computed: {
            balloonTemplate() {
                return `
                    <a href="/developers/developer/object" class="buildCard">
                        <h6 class="buildName">ЖК Фергана</h6>
                        <div class="buildImage">
                            <img src="https://mirabad.uz/upload/kelnik.adminpage/c0c/c0cf81c2a22ec8ec0c77335fe14b9533.jpg"/>
                        </div>
                        <span class="buildText">880 квартир До 18 Этажей Квартиры от 52 м2 Начало строительства 2018 год</span>
                    </a>
                `
            }
        }
    }
</script>

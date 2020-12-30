<template>
    <div>
        <div class="pt-5" style="background: rgba(0, 66, 116, 1);">
            <b-row class="m-0 mb-5">
            <b-col cols="3">
                <h5 class="text-white">О сайте</h5>
                <div class="text-light">
                <small>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam illum eveniet pariatur, inventore dicta fuga qui doloremque? Iusto at explicabo doloribus dolorem soluta perferendis eveniet exercitationem corporis aperiam! Ipsum, repellendus.
                </small>
                </div>
            </b-col>
            <b-col cols="3">
                <h5 class="text-white">Свяжитесь с нами</h5>
                <b-nav vertical>
                <nuxt-link to="/" class="text-light text-decoration-none">
                    <img src="@/assets/images/svg/message.svg" class="mr-2" style="width: 15px; height: 15px;" alt="">
                    <small>info@domtut.uz</small>
                </nuxt-link>
                <nuxt-link to="/" class="text-light text-decoration-none">
                    <img src="@/assets/images/svg/telegram.svg" class="mr-2" style="width: 15px; height: 15px;" alt="">
                    <small>Мы в Telegram</small>
                </nuxt-link>
                <nuxt-link to="/" class="text-light text-decoration-none">
                    <img src="@/assets/images/svg/facebook.svg" class="mr-2" style="width: 15px; height: 15px;" alt="">
                    <small>Мы в Facebook</small>
                </nuxt-link>
                <nuxt-link to="/" class="text-light text-decoration-none">
                    <img src="@/assets/images/svg/instagram.svg" class="mr-2" style="width: 15px; height: 15px;" alt="">
                    <small>Мы в Instagram</small>
                </nuxt-link>
                <nuxt-link to="/" class="text-light text-decoration-none">
                    <img src="@/assets/images/svg/twitter.svg" class="mr-2" style="width: 15px; height: 15px;" alt="">
                    <small>Мы в Twitter</small>
                </nuxt-link>
                </b-nav>
            </b-col>
            <b-col cols="2">
                <div class="text-light mb-1"><small>Квартиры</small></div>
                <div class="text-light"><small>1-комнатные</small></div>
                <div class="text-light"><small>2-комнатные</small></div>
                <div class="text-light"><small>3-комнатные</small></div>
                <div class="text-light"><small>4-комнатные</small></div>
                <div class="text-light"><small>5-комнатные</small></div>
            </b-col>
            <b-col cols="2">
                <div class="text-light mb-1"><small>Стоимость</small></div>
                <div class="text-light"><small>До 300 млн</small></div>
                <div class="text-light"><small>До 500 млн</small></div>
                <div class="text-light"><small>До 800 млн</small></div>
                <div class="text-light"><small>Более 800 млн</small></div>
                <div class="text-light"><small>С отделкой</small></div>
                <div class="text-light"><small>Без отделки</small></div>
            </b-col>
            <b-col cols="2">
                <div class="text-light mb-1"><small>Квадратура</small></div>
                <div class="text-light"><small>Квартиры до 50 м²</small></div>
                <div class="text-light"><small>Квартиры от 50 м² до 75 м²</small></div>
                <div class="text-light"><small>Квартиры от 75 м² до 100 м²</small></div>
                <div class="text-light"><small>Квартиры больше 100 м²</small></div>
                <div class="text-light"><small>Квартиры больше 200 м²</small></div>
            </b-col>
            </b-row>
            <div class="text-right pb-3">
            <b-button variant="warning" class="px-2 pb-2 pt-1">
                <img src="@/assets/images/svg/upwards-arrow.svg" style="width: 20px; height: 20px;" alt="">
            </b-button>
            </div>
        </div>
    </div>
</template>
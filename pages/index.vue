<template>
<div>
  <Header />  
  
  <b-container class="mt-5">
    <b-row class="bg-light p-2 mb-5">
      <b-col cols="3" class="py-2 px-2" v-for="i in 2" :key="i">
        <div class="bg-white" style="box-shadow: 0px 10px 15px 2px rgba(202, 202, 202, 0.2);">
          <div class="position-relative">
            <div class="d-flex pb-1 px-2 m-1 rounded align-items-center position-absolute" style="background: rgba(0, 0, 0, .6);">
              <img src="@/assets/images/svg/star.svg" class="mt-1" style="width: 10px; height: 10px; line-height: 0;" alt="">
              <span class="text-white font-weight-bold ml-1"><small>4.4</small></span>
              <img src="@/assets/images/svg/comment.svg" class="ml-2 mt-2" style="width: 15px; height: 15px; line-height: 0;" alt="">
              <span class="text-white font-weight-bold ml-1"><small>18</small></span>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="right: 0;">
              <b-button size="sm" variant="transparent" style="background: rgba(255, 255, 255, .6);">
                <img src="@/assets/images/svg/add-list.svg" style="width: 15px; height: 15px;" alt="">
              </b-button>
              <b-button size="sm" variant="transparent" style="background: rgba(255, 255, 255, 1);" class="ml-2">
                <img src="@/assets/images/svg/like.svg" style="width: 15px; height: 15px;" alt="">
              </b-button>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="left: 0; bottom: 0;">
              <div class="d-flex">
                <b-button variant="danger" class="rounded-circle py-1">
                  <img src="@/assets/images/svg/percent.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt="">
                </b-button>
                <b-button variant="primary" class="rounded-circle py-1" style="margin-left: -10px;">
                  <img src="@/assets/images/svg/home.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt=""
                ></b-button>
                <b-button variant="info" class="rounded-circle py-1" style="margin-left: -10px;">
                  <img src="@/assets/images/svg/hourglass.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt="">
                </b-button>
              </div>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="right: 0; bottom: 0;">
              <b-button size="sm" variant="transprent" pill class="border-light text-white text-uppercase" style="background: rgba(0, 0, 0, .6);">
                <small>Поэтажный план</small>
              </b-button>
            </div>
            <img src="https://q4g9y5a8.rocketcdn.me/wp-content/uploads/2020/02/home-banner-2020-02-min.jpg" style="width: 100%;" alt="">
            
          </div>
          <div class="p-2">
            <div class="d-flex justify-content-between">
              <div class="text-secondary"><small>INGRAD (Инград)</small></div>
              <div class="text-warning"><small>Строится</small></div>
              <div class="text-success"><small>Есть сданные</small></div>
            </div>
            <div class="text-primary font-weight-bold mb-4">ЖК RiverSky (РиверСкай)</div>
            <small>Москва, ЮАО</small>
            <small class="d-flex align-items-center mb-2">
              <li class="active-li">Автозаводская</li> 
              <img src="@/assets/images/svg/man-hugging.svg" class="ml-2" style="width: 10px; height: 10px; line-height: 0;" alt="">
              9 мин
            </small>
            <div class="d-flex justify-content-between">
              <small>1-комн. <span class="text-secondary">от 38.70 м²</span></small>
              <small>15 374 542 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>2-комн. <span class="text-secondary">от 45.96 м²</span></small>
              <small>17 977 943 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>3-комн. <span class="text-secondary">от 85.89 м²</span></small>
              <small>26 768 945 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>4-комн. <span class="text-secondary">от 101.85 м²</span></small>
              <small>39 509 142 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between mt-3">
              <div class="font-weight-bold text-primary">115 квартир</div>
              <div class="text-primary">от 76 749 Ꝑ/мес</div>
            </div>
          </div>
        </div>
      </b-col>
      <b-col cols="3" class="py-2 px-2" v-for="i in 2" :key="i">
        <div class="bg-white" style="box-shadow: 0px 10px 15px 2px rgba(202, 202, 202, 0.2);">
          <div class="position-relative">
            <div class="d-flex pb-1 px-2 m-1 rounded align-items-center position-absolute" style="background: rgba(0, 0, 0, .6);">
              <img src="@/assets/images/svg/star.svg" class="mt-1" style="width: 10px; height: 10px; line-height: 0;" alt="">
              <span class="text-white font-weight-bold ml-1"><small>4.4</small></span>
              <img src="@/assets/images/svg/comment.svg" class="ml-2 mt-2" style="width: 15px; height: 15px; line-height: 0;" alt="">
              <span class="text-white font-weight-bold ml-1"><small>18</small></span>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="right: 0;">
              <b-button size="sm" variant="transparent" style="background: rgba(255, 255, 255, .6);">
                <img src="@/assets/images/svg/add-list.svg" style="width: 15px; height: 15px;" alt="">
              </b-button>
              <b-button size="sm" variant="transparent" style="background: rgba(255, 255, 255, 1);" class="ml-2">
                <img src="@/assets/images/svg/like.svg" style="width: 15px; height: 15px;" alt="">
              </b-button>
              <b-button size="sm" variant="transparent" style="background: rgba(255, 255, 255, .6);" class="ml-2">
                <img src="@/assets/images/svg/call.svg" style="width: 15px; height: 15px;" alt="">
              </b-button>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="left: 0; bottom: 0;">
              <div class="d-flex">
                <b-button variant="danger" class="rounded-circle py-1">
                  <img src="@/assets/images/svg/percent.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt="">
                </b-button>
                <b-button variant="primary" class="rounded-circle py-1" style="margin-left: -10px;">
                  <img src="@/assets/images/svg/home.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt=""
                ></b-button>
                <b-button variant="warning" class="rounded-circle py-1" style="margin-left: -10px;">
                  <img src="@/assets/images/svg/guarantee.svg" class="mb-1" style="width: 12px; height: 15px; line-height: 0;" alt="">
                </b-button>
              </div>
            </div>
            <div class="d-flex py-1 px-2 mr-0 position-absolute" style="right: 0; bottom: 0;">
              <b-button size="sm" variant="transprent" pill class="border-light text-white text-uppercase" style="background: rgba(0, 0, 0, .6);">
                <small>Поэтажный план</small>
              </b-button>
            </div>
            <img src="https://q4g9y5a8.rocketcdn.me/wp-content/uploads/2020/02/home-banner-2020-02-min.jpg" style="width: 100%;" alt="">
            
          </div>
          <div class="p-2">
            <div class="d-flex justify-content-between">
              <div class="text-secondary"><small>INGRAD (Инград)</small></div>
              <div class="text-warning"><small>Строится</small></div>
            </div>
            <div class="text-primary font-weight-bold mb-4">ЖК RiverSky (РиверСкай)</div>
            <small>Москва, ЮАО</small>
            <small class="d-flex align-items-center mb-2">
              <li class="disactive-li">Автозаводская</li> 
              <img src="@/assets/images/svg/man-hugging.svg" class="ml-2" style="width: 10px; height: 10px; line-height: 0;" alt="">
              9 мин
            </small>
            <div class="d-flex justify-content-between">
              <small>1-комн. <span class="text-secondary">от 38.70 м²</span></small>
              <small>15 374 542 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>2-комн. <span class="text-secondary">от 45.96 м²</span></small>
              <small>17 977 943 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>3-комн. <span class="text-secondary">от 85.89 м²</span></small>
              <small>26 768 945 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between">
              <small>4-комн. <span class="text-secondary">от 101.85 м²</span></small>
              <small>39 509 142 Ꝑ</small>
            </div>
            <div class="d-flex justify-content-between mt-3">
              <div class="font-weight-bold text-primary">115 квартир</div>
              <div class="text-primary">от 76 749 Ꝑ/мес</div>
            </div>
          </div>
        </div>
      </b-col>
    </b-row>
  </b-container>
  <b-container class="mb-5 text-center w-100">
    <div class="p-4 bg-light w-50 mx-auto">
      <b-button variant="outline-primary" class="px-5">Показать ещё</b-button>
      <div class="mt-4">
        <b-pagination v-model="currentPage" pills :total-rows="rows" align="center" class="mb-0"></b-pagination>
      </div>
    </div>
  </b-container>
  
  <Footer />
  
</div>
</template>

<script>
import Header from '@/components/header'
import Footer from '@/components/footer'

  export default {
    data() {
      return {
        rows: 100,
        currentPage: 1
      }
    }
  }
</script>

<style>
li {
  list-style: none; 
}
li.disactive-li::before {
  content: "";
  color: grey;
  font-weight: bold;
  display: inline-block;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  margin-right: 5px;
  background: grey;
}
li.active-li::before {
  content: "";
  color: grey;
  font-weight: bold;
  display: inline-block;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  margin-right: 5px;
  background: green;
}
</style>

<template>
<div>


  <div class=""></div>

  <Header />  
  
  <div>
    <div class="bestsellers">
      <div class="container_1290">
        <div class="d-flex">
          <div class="bestsellers__title">Хиты продаж</div>        
          <nuxt-link to="/" class="bestsellers__seeAll text-decoration-none">367</nuxt-link>
        </div>
        <div class="d-flex flex-wrap bestsellers__cards">
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 52.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textDisactive">Строиться</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 53.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textActive">Построено</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 54.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textDisactive">Строиться</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 55.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textDisactive">Строиться</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 56.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textActive">Построено</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 57.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textActive">Построено</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 58.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textActive">Построено</div>
              </div>
            </div>
          </div>
          <div class="card">
            <div class="card__image">
              <img src="@/assets/images/png/cards/image 59.png">
            </div>
            <div class="card__image_bg"></div>
            <div class="card__content_top d-flex justify-content-between align-items-top">
              <div>
                <div class="card__companyName">BudCapital</div>
                <div class="card__buildName">ЖК Star City</div>
              </div>
              <div class="card__rating d-flex">
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/star.svg"></div>
                  <div class="card__rating_text">4.5</div>
                </div>
                <div class="d-flex align-items-center">
                  <div class="card__rating_image"><img src="@/assets/images/svg/card-icons/message.svg"></div>
                  <div class="card__rating_text">25</div>
                </div>
              </div>
            </div>
            <div class="card__content_bottom">
              <b-button variant="transparent" class="card__btnStay shadow-none">Осталось - 100 квартир</b-button>
              <div class="card__price">от <span>2.07</span> млн сум м2</div>
              <div class="card__status d-flex justify-content-between">
                <div class="d-flex">
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/discount.svg">
                    <span class="card__status_tooltip">В рассрочку</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/clock.svg">
                    <span class="card__status_tooltip">Время</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/key.svg">
                    <span class="card__status_tooltip">Под ключ</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/warranty.svg">
                    <span class="card__status_tooltip">Гарантия</span>
                  </div>
                  <div class="card__status_image">
                    <img src="@/assets/images/svg/card-icons/without_finishing.svg">
                    <span class="card__status_tooltip">Без отделки</span>
                  </div>
                </div>
                <div class="card__status_text card__status_textDisactive">Строиться</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- <b-container class="mb-5 text-center w-100">
    <div class="p-4 bg-light w-50 mx-auto">
      <b-button variant="outline-primary" class="px-5">Показать ещё</b-button>
      <div class="mt-4">
        <b-pagination v-model="currentPage" pills :total-rows="rows" align="center" class="mb-0"></b-pagination>
      </div>
    </div>
  </b-container>  -->
  
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
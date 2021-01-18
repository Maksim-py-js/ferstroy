<template>
<div>  
  <b-container class="position-relative">
    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d95913.44056607499!2d69.23376702582306!3d41.30244525704403!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2s!4v1609333243458!5m2!1sru!2s" width="1140" height="707" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
    <div class="position-absolute h-100 bg-white p-3" style="top: 0; right: 0; width: 310px;">
        <div class="mb-2">
            <b-button variant="light" class="mr-1 mb-1">Москва и МО</b-button>
            <b-button variant="light" class="mr-1 mb-1">Москва</b-button>
            <b-button variant="light" class="mr-1 mb-1">Подмосковье</b-button>
            <b-button variant="light" class="mr-1 mb-1">Новая Москва</b-button>
            <b-button variant="light" class="mr-1 mb-1">Санкт Петербург</b-button>
        </div>
        <div>
            <div class="text-secondary"><small>Цена</small></div>
            <div class="d-flex mt-2">          
                <b-form class="d-flex">
                    <b-form-group class="mr-1">
                    <b-form-input
                        id="input-1"
                        type="number"
                        placeholder="от 0 млн"
                        required
                    ></b-form-input>
                    </b-form-group>
                    <b-form-group>
                    <b-form-input
                        id="input-1"
                        type="number"
                        placeholder="до 850 млн"
                        required
                    ></b-form-input>
                    </b-form-group>
                </b-form>
            </div>
        </div>
        <div>
            <label for="range-2" class="text-secondary"><small>Срок сдачи</small></label>
            <b-form-input id="range-2" v-model="map_deadlineRangeValue" type="range" min="2020" max="2024" step="1"></b-form-input>
            <div class="mt-2">{{ map_deadlineRangeValue }}</div>
        </div>
        <div class="mt-3">
            <div class="text-secondary mb-2"><small>Студия</small></div>
            <b-form-select v-model="map_selected_roominessOptions" :options="map_roominessOptions"></b-form-select>
        </div>
        <div>
            <div class="text-secondary"><small>Площадь</small></div>
            <div class="d-flex mt-2">          
                <b-form class="d-flex">
                    <b-form-group class="mr-1">
                    <b-form-input
                        id="input-1"
                        type="number"
                        placeholder="от 20 м²"
                        required
                    ></b-form-input>
                    </b-form-group>
                    <b-form-group>
                    <b-form-input
                        id="input-1"
                        type="number"
                        placeholder="до 200 м²"
                        required
                    ></b-form-input>
                    </b-form-group>
                </b-form>
            </div>
        </div>
        <div class="mb-2">
            <b-button variant="light" class="mr-1 mb-1">Квартиры</b-button>
            <b-button variant="light" class="mr-1 mb-1">Апартаменты</b-button>
            <b-button variant="light" class="mr-1 mb-1">Танхаусы</b-button>
        </div>
    </div>
  </b-container>
</div>
</template>

<script>
  export default { 
    layout: 'main',
    data() {
      return {
        map_deadlineRangeValue: 'Сдана',
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
        ]
      }
    }
  }
</script>

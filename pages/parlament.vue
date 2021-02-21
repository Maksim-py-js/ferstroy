<template>
    <div class="h-panel p-4">
        <div class="background-filter"></div>  
        <b-navbar class="panel-top p-0 mb-4">
            <!-- Right aligned nav items -->
            <b-navbar-nav class="d-flex align-items-center justify-content-between w-100">
                <!-- <b-breadcrumb variant="transparent" :items="bredcrumbsItems" class="custom-breadcrumbs mb-0 bg-transparent text-light"></b-breadcrumb> -->
                <nuxt-link to="/" class="header__logo">
                    <img src="@/assets/images/svg/logo/russian-light.svg">
                </nuxt-link>
                <div class="position-relative header__language">
                    <div class="header__language_block position-absolute">
                        <b-button variant="transparent" class="header__language_btn shadow-none">Рус</b-button>
                        <b-button variant="transparent" class="header__language_btn shadow-none">Узб</b-button>
                    </div>
                </div>
            </b-navbar-nav>
        </b-navbar>
        <b-row class="m-0">
            <b-col cols="2" class="tabs p-0">
                <b-nav vertical v-for="item in tabsItem" :key="item.id">                
                    <b-nav-item 
                        :to="item.path" 
                        class="tabs-item pl-0 pt-2 pb-2" 
                        :class="{active:item.active}"
                    >   
                        {{item.name}}
                    </b-nav-item>
                </b-nav>
            </b-col>
            <b-col class="bg-light w-100 p-0">                
                <nuxt-child />
                <notifications group="admin-notification"/>
            </b-col>
        </b-row>
    </div>
</template>

<!-- @click="item.active = !item.active" -->
<script>
  export default {
    data() {
      return {
        active: true,
        tabsItem: [
            {
                id: 1,
                path: "/parlament/developer_users",
                name: 'Застройщики',
                active: false
            },
            {
                id: 2,
                path: "/parlament/area",
                name: 'Жилые комплексы',
                active: false
            },
            {
                id: 3,
                path: "/parlament/buildings",
                name: 'Здания',
                active: false
            }
        ],
        bredcrumbsItems: [
          {
            text: 'Главная',
            href: '/'
          },
          {
            text: 'Хокимиат',
            active: true
          }
        ]
      }
    }
  }
</script>

<style>
    .h-panel {
        background: url('../assets/images/png/slide_1-min.png') no-repeat 50% 50%/cover;
        position: relative;
        transition: 0.5s;
    }
    .background-filter {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background: linear-gradient(180deg, rgba(0, 0, 0, 0.7) 0%, rgba(0, 0, 0, 0.8) 34.9%);
        transition: 0.5s;
    }
    .panel-top .header__language_block:hover {
        height: 56px;
        transition: 0.5s;
    }
    .tabs {
        max-width: 220px;
        width: 100%;
        height: 100vh;
        transition: 0.5s;
    }
    .tabs-item a{
        color: #fff;
        font-family: "Montserrat";
        font-size: 18px;
        font-weight: 400;
        padding: 0;
        transition: 0.5s;
    }
    .tabs-item a:hover, .tabs-item.active a {
        color: #FF9800;
        transition: 0.5s;
    }
</style>
<template>
    <div class="wrapper">
        <div class="header-wrapper hidden-sm-and-down white">
      <div id="header" />
      <v-row class="header white">
        <v-col cols="4" class="logo-wrapper">
            <nuxt-link to="/" style="width: 100% ">
          <v-img src="/flatwood.png" contain class="logo-image" />
        </nuxt-link>
        </v-col>
        <v-col class="menu-wrapper">
          <ul class="menu-list">
            
            <li class="menu-text"><nuxt-link :to="{path: '/', hash: '#production'}" class="menu-text">производство</nuxt-link></li>
            <li class="menu-text"><nuxt-link  :to="{path: '/', hash: '#models'}" class="menu-text">модельный ряд</nuxt-link></li>
            <li class="menu-text"><nuxt-link :to="{path: '/', hash: '#team'}" class="menu-text">команда</nuxt-link></li>
            <li class="menu-text">что дальше</li>
          </ul>
        </v-col>
      </v-row>
    </div>
    <div class="header-wrapper hidden-sm-and-up white">
      <div id="header-mobile" />
      <v-row class="header-mobile white">
        <v-col cols="8" class="logo-wrapper-mobile">
          <v-img src="/flatwood.png" contain class="logo-image-mobile" />
        </v-col>
        <v-col cols="4" class="d-flex justify-end">
            <v-btn elevation="0" color="transparent" @click="menuVisible=true">
              <v-img src="/hamburger.svg"></v-img>
            </v-btn>
        </v-col>
      </v-row>
    </div>

<div class="main-info-wrapper hidden-sm-and-down">
    <v-col cols="6">
            <v-img :src="images[currentImageIndex]" width="650" height="426" contain class="main-img">
                <v-btn fab elevation="0" color="#f6f6f6" class="magnify-btn" @click="lightBoxVisible=true">
                    <v-icon>mdi-magnify-plus-outline</v-icon>
                </v-btn>
            </v-img>
            <v-row class="img-minis-row">
                <v-img contain :class="idx===currentImageIndex ? 'img-mini-active' : 'img-mini'" v-for="(img, idx) in images" :key="idx" :src="img" @click="changeMainImage(idx)"></v-img>
            </v-row>
    </v-col>
    <v-col cols="6" class="product-info-col">
        <nuxt-link :to="{path: '/', hash: '#models'}" class="footer-menu-item"><span class="back-link-text">Вернуться на главную</span></nuxt-link>
        <span class="product-header-text">карл четырехногий</span>
        <span class="product-descr-text">Поэтому достаточное условие сходимости стремительно восстанавливает абстрактный интеграл по ориентированной области. Открытое множество решительно накладывает параллельный бином Ньютона.
Согласно последним исследованиям, интеграл Пуассона трансформирует стремящийся интеграл Дирихле. Можно предположить, что предел последовательности нейтрализует интеграл Фурье.</span>
        <a href="https://ozon.ru" style="text-decoration: none"><span class="h-button heading-h3 h-button-text">купить на ozon.ru</span></a></a>
    </v-col>
</div>

<div class="main-info-wrapper-mobile hidden-sm-and-up">
    <v-col cols="12" class="py-4 product-image-col-mobile" >
        <nuxt-link :to="{path: '/', hash: '#models'}" class="footer-menu-item"><span class="back-link-text">Вернуться на главную</span></nuxt-link>
        <span class="mobile-h1">карл четырехногий</span>
            <v-img :src="images[currentImageIndex]" width="650" height="auto" contain class="main-img">
                <v-btn fab elevation="0" color="#f6f6f6" class="magnify-btn" @click="lightBoxVisible=true">
                    <a href="https://ozon.ru" style="text-decoration: none !important"></a><v-icon>mdi-magnify-plus-outline</v-icon>
                </v-btn>
            </v-img>
            <v-row class="img-minis-row">
                <v-slide-group
      v-model="model"
      class="py-4"
      mandatory
    >
    
      <v-slide-item
        v-slot="{ active, toggle }"
        v-for="(img, idx) in images" :key="idx"
      >
      
<div @click="toggle">
    <v-img :class="idx===currentImageIndex ? 'img-mini-active mr-1' : 'img-mini mr-1'"  :src="img" @click="changeMainImage(idx)"></v-img>

</div>
      </v-slide-item>
    </v-slide-group>
            </v-row>
    </v-col>
    <v-col cols="12" class="product-info-col">
       
        <span class="product-descr-text">Поэтому достаточное условие сходимости стремительно восстанавливает абстрактный интеграл по ориентированной области. Открытое множество решительно накладывает параллельный бином Ньютона.
Согласно последним исследованиям, интеграл Пуассона трансформирует стремящийся интеграл Дирихле. Можно предположить, что предел последовательности нейтрализует интеграл Фурье.</span>
<a href="https://ozon.ru" style="text-decoration: none !important"> <span class="hero-mobile-button mobile-h3 h-button-text">купить на ozon.ru</span></a>
    </v-col>

</div>

<div class="footer-wrapper hidden-sm-and-down">
      <div class="footer inner-section">
        <v-row class="align-center footer-row">
          <v-col>© 2022 Flatwood</v-col>
          <v-col>
            <ul class="menu-list">
              <li class="footer-menu-item"><nuxt-link :to="{path: '/', hash: '#production'}" class="footer-menu-item">Производство</nuxt-link></li>
              <li class="footer-menu-item"><nuxt-link  :to="{path: '/', hash: '#models'}" class="footer-menu-item">Модельный ряд</nuxt-link></li>
              <li class="footer-menu-item"><nuxt-link :to="{path: '/', hash: '#team'}" class="footer-menu-item">Команда</nuxt-link></li>
              <li class="footer-menu-item">Что дальше</li>
            </ul>
          </v-col>
        </v-row>
      </div>
    </div>
    <div class="footer-wrapper-mobile hidden-sm-and-up">
      <div class="footer-mobile inner-section-mobile">
        <div class="align-center footer-row-mobile">
          <v-col class="footer-mobile-copyright">© 2022 Flatwood</v-col>
          <v-col class="d-flex footer-mobile-menu-col" style="gap: 1rem;">
            <ul class="menu-footer-mobile">
              <li class="footer-mobile-menu-item">Производство</li>
              <v-divider />
              <li class="footer-mobile-menu-item">Модельный ряд</li>
              <v-divider />
              <li class="footer-mobile-menu-item">Команда</li>
              <v-divider />
              <li class="footer-mobile-menu-item">Что дальше</li>
            </ul>
          </v-col>
        </div>
      </div>
    </div>
    
    <v-dialog persistent fullscreen content-class="mobile-menu-container" v-model="menuVisible">
      <ul class="menu-mobele-list">
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#production-mobile'}" class="menu-mobile-item-text" >производство</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#models-mobile'}" class="menu-mobile-item-text" >модельный ряд</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#team-mobile'}" class="menu-mobile-item-text" >команда</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false">что дальше</li>
          </ul>
          <v-fab rounded="10" class="mobile-menu-close-button" @click="menuVisible=false">
            <v-icon class="mobile-menu-close-button" large>mdi-close</v-icon>
          </v-fab>
    </v-dialog>
    <v-dialog  overlay-opacity="0.8" persistent v-model="lightBoxVisible" content-class="lightbox" >
            <v-btn fab absolute  class="lb-close-button" @click="lightBoxVisible=false"><v-icon>mdi-close</v-icon></v-btn>
            <v-row class="hidden-sm-and-up mx-0">
               
                <v-col cols="12" class="lb-center-column">
                    <v-img :src="images[currentLightBoxIndex]"  class="lb-center-img" contain></v-img>
                </v-col>
               <v-row>
                <v-col cols="6" class="lb-nav-column-left">
                    <v-btn fab elevation="0" @click="lightboxPrev" color="#DB8E5A"><v-icon color="white">mdi-chevron-left</v-icon></v-btn>
                </v-col>
                <v-col cols="6" class="lb-nav-column-right">
                    <v-btn fab elevation="0" @click="lightboxNext" color="#DB8E5A"><v-icon color="white">mdi-chevron-right</v-icon></v-btn>
                </v-col>
               </v-row>
            </v-row>
            <v-row class="hidden-sm-and-down">
                <v-col cols="1" class="lb-nav-column-right">
                    <v-btn fab elevation="0" @click="lightboxPrev"><v-icon>mdi-chevron-left</v-icon></v-btn>
                </v-col>
                <v-col cols="10" class="lb-center-column">
                    <v-img :src="images[currentLightBoxIndex]"  class="lb-center-img" contain></v-img>
                </v-col>
                <v-col cols="1" class="lb-nav-column-left">
                    <v-btn fab elevation="0" @click="lightboxNext"><v-icon>mdi-chevron-right</v-icon></v-btn>
                </v-col>
            </v-row>
    </v-dialog>
    </div>
</template>

<script>
export default {
    data() {
        return {
            model: 0,
            menuVisible: false,
            images: [
                '/tt11.jpg',
                '/models1.png',
                '/product1.png',
                '/galary1.png',
            ],
            currentImageIndex: 0,
            lightBoxVisible: false,
            currentLightBoxIndex: 0,
        }
    },
    methods: {
        changeMainImage(idx) {
            this.currentImageIndex=idx
        },
        lightboxNext() {
            //console.log(this.currentLightBoxIndex);
            if (this.currentLightBoxIndex>=this.images.length-1) {
                console.log('piccc');
                this.currentLightBoxIndex=0
                console.log(this.currentLightBoxIndex);
                return
            }
            this.currentLightBoxIndex = this.currentLightBoxIndex + 1
            console.log(this.currentLightBoxIndex);

        },
        lightboxPrev() {
            if (this.currentLightBoxIndex-1<0) {
                this.currentLightBoxIndex=this.images.length-1
                return
            }
            this.currentLightBoxIndex = this.currentLightBoxIndex  - 1
        }
    }
}
</script>

<template>
  <div class="wrapper">
    <div id="top" />
    <div class="header-wrapper hidden-sm-and-down">
      <div id="header" />
      <v-row class="header">
        <v-col cols="4" class="logo-wrapper">
          <nuxt-link to="/" style="width: 100%">
          <v-img src="/flatwood.png" contain class="logo-image" />
        </nuxt-link>
        </v-col>
        <v-col class="menu-wrapper">
          <ul class="menu-list">
            <li class="menu-text"><nuxt-link :to="{path: '/', hash: '#production'}" class="menu-text">производство</nuxt-link></li>
            <li class="menu-text"><nuxt-link  :to="{path: '/', hash: '#models'}" class="menu-text">модельный ряд</nuxt-link></li>
            <li class="menu-text"><nuxt-link :to="{path: '/', hash: '#team'}" class="menu-text">команда</nuxt-link></li>
            <li class="menu-text"><nuxt-link :to="{path: '/', hash: '#contacts'}" class="menu-text">Контакты</nuxt-link></li>
          </ul>
        </v-col>
      </v-row>
    </div>
    <div class="header-wrapper hidden-sm-and-up">
      <div id="header-mobile" />
      <v-row class="header-mobile">
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
    <div class="hero-wrapper hidden-sm-and-down">
      <v-row class="hero">
        <v-col cols="5" class="h-left">
          <span class="heading-h1">привет, я — стол</span>
          <span class="heading-m-light-desktop"
            >Интеграл Фурье, следовательно, реально <br />
            накладывает криволинейный интеграл. Нечетная<br />
            функция естественно привлекает интеграл по поверхности. Скалярное
            произведение изменяет математический анализ.</span
          >
          <a href="https://ozon.ru" style="text-decoration: none"><span class="h-button heading-h3 h-button-text">купить меня</span></a>
        </v-col>
        <v-col cols="7" class="h-right">
          <v-img src="/intro_table.png" class="intro-image" width="1000" />
        </v-col>
      </v-row>
    </div>
    <div class="hero-wrapper-mobile hidden-sm-and-up">
      <v-row >
        <v-col cols="12" >
          <v-img src="/intro_table.png"  width="1000" />
        </v-col>
        <v-col cols="12" class="hero-mobile-text">
          <span class="mobile-h1">привет, я — стол</span>
          <span class="heading-m-light-mobile"
            >Интеграл Фурье, следовательно, реально 
            накладывает криволинейный интеграл. Нечетная
            функция естественно привлекает интеграл по поверхности. Скалярное
            произведение изменяет математический анализ.</span>
            <a href="https://ozon.ru" style="text-decoration: none"><span class="hero-mobile-button heading-h3 h-button-text">купить меня</span></a>
        </v-col>
        
      </v-row>
    </div>
    <div class="galery-wrapper hidden-sm-and-down">
      <v-row class="galery">
        <v-card elevation="0" rounded="0" class="galery-item" max-width="32%">
          <v-img src="/galary1.png" contain></v-img>
          <span class="heading-h2">я в интерьере</span>
          <span class="heading-s-regular-desktop"
            >Интеграл Фурье, следовательно, реально накладывает криволинейный
            интеграл. Нечетная функция естественно привлекает интеграл по
            поверхности.</span
          >
        </v-card>
        <v-card elevation="0" rounded="0" class="galery-item" max-width="32%">
          <v-img src="/galary2.png" cover></v-img>
          <span class="heading-h2">детали</span>
          <span class="heading-s-regular-desktop"
            >Интеграл Фурье, следовательно, реально накладывает криволинейный
            интеграл. Нечетная функция естественно привлекает интеграл по
            поверхности.</span
          >
        </v-card>
        <v-card elevation="0" rounded="0" class="galery-item" max-width="32%">
          <v-img src="/galary3.png" cover></v-img>
          <span class="heading-h2">материалы</span>
          <span class="heading-s-regular-desktop"
            >Интеграл Фурье, следовательно, реально накладывает криволинейный
            интеграл. Нечетная функция естественно привлекает интеграл по
            поверхности.</span
          >
        </v-card>
      </v-row>
    </div>
    <div class="galery-mobile-wrapper hidden-sm-and-up">
   
    <v-slide-group
      v-model="model"
      class="py-4 pl-3"
      center-active
      mandatory
    >
      <v-slide-item
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? 'transparent' : 'transparen'"
          height="450"
          width="285"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
          <v-img src="/galary1.png" cover width="100%" height="214px"></v-img>
          <span class="mobile-h2">я в интерьере</span>
          <span class="heading-s-regular-mobile"
            >Интеграл Фурье, следовательно,<br/>реально накладывает<br/> криволинейный
            интеграл.<br/> Нечетная функция естественно<br/> привлекает интеграл по<br/>
            поверхности.</span
          >
        </v-col>
        </v-card>
      </v-slide-item>
      <v-slide-item
        v-slot="{ active, toggle }"
      >
      
        <v-card
          :color="active ? 'white' : 'white'"
          height="450"
          width="285"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
        <v-img src="/galary2.png" cover width="100%" height="214px"></v-img>
          <span class="mobile-h2">детали</span>
          <span class="heading-s-regular-mobile"
            >Интеграл Фурье, следовательно,<br/>реально накладывает<br/> криволинейный
            интеграл.<br/> Нечетная функция естественно<br/> привлекает интеграл по<br/>
            поверхности.</span
          >
        </v-col>
        </v-card>
      </v-slide-item>
      <v-slide-item
        v-slot="{ toggle }"
      >
        <v-card
          height="450"
          width="285"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
        <v-img src="/galary3.png" cover width="100%" height="214px"></v-img>
          <span class="mobile-h2">материалы</span>
          <span class="heading-s-regular-mobile"
            >Интеграл Фурье, следовательно,<br/>реально накладывает<br/> криволинейный
            интеграл.<br/> Нечетная функция естественно<br/> привлекает интеграл по<br/>
            поверхности.</span
          >
        </v-col>
        </v-card>
      </v-slide-item>
    </v-slide-group>

    </div>
    <div class="production-wrapper hidden-sm-and-down">
      <div id="production" />
      <div class="production inner-section">
        <v-row>
          <v-img src="/production.png" />
        </v-row>
        <v-row style="margin-top: 2.5rem">
          <v-col cols="3" class="production-item heading-h2"
            >Производство</v-col
          >
          <v-col cols="9" class="production-item heading-m-light-desktop"
            >Сумма ряда, конечно, накладывает неопределенный интеграл, что и
            требовалось доказать. Интеграл Дирихле, следовательно,
            трансформирует полином. Метод последовательных приближений, исключая
            очевидный случай, стабилизирует постулат. Огибающая существенно
            упорядочивает неопровержимый интеграл Пуассона, что и требовалось
            доказать. Функция B(x,y) непосредственно концентрирует лист
            Мёбиуса</v-col
          >
        </v-row>
      </div>
    </div>
    <div class="production-mobile-wrapper hidden-sm-and-up">
      <div id="production-mobile" />
      <div class="production inner-section">
          <v-img src="/production.png" width="94%" height="400px" cover class="production-mobile-image"/>
        <div style="margin-top: 2.5rem; margin-left: 1rem;">
          <v-col cols="3" class="production-item mobile-h2"
            >Производство</v-col
          >
          <v-col cols="12" class="production-item heading-m-light-mobile"
            >Сумма ряда, конечно, накладывает неопределенный интеграл, что и
            требовалось доказать. Интеграл Дирихле, следовательно,
            трансформирует полином. Метод последовательных приближений, исключая
            очевидный случай, стабилизирует постулат. Огибающая существенно
            упорядочивает неопровержимый интеграл Пуассона, что и требовалось
            доказать. Функция B(x,y) непосредственно концентрирует лист
            Мёбиуса</v-col
          >
        </div>
      </div>
    </div>
    <div class="models-wrapper hidden-sm-and-down">
      <div id="models" />
      <div class="models inner-section">
        <span class="models-header heading-h2">модельный ряд</span>
        <v-row class="models-row">
          <v-card elevation="0" rounded="0" class="models-card">
            <div class="models-card-image-wrapper">
              <v-img src="/tt11.jpg"  width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table', hash: '#top'}" class="heading-h3 models-card-link"><span class="heading-h3 models-card-link">карл четырехногий →</span></nuxt-link>
            
            <span class="heading-s-regular-desktop  mt-2"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
          </v-card>
          <v-card elevation="0" rounded="0" class="models-card">
            <div class="models-card-image-wrapper">
              <v-img src="/tt2.jpg"  width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table1', hash: '#top'}" class="heading-h3 models-card-link"><span class="heading-h3 models-card-link">плоский джо →</span></nuxt-link>
            <span class="heading-s-regular-desktop  mt-2"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
          </v-card>
          <v-card elevation="0" rounded="0" class="models-card">
            <div class="models-card-image-wrapper">
              <v-img src="/tt44.jpg" width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table2', hash: '#top'}" class="heading-h3 models-card-link"><span class="heading-h3 models-card-link">дубовый багет →</span></nuxt-link>
            <span class="heading-s-regular-desktop  mt-2"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
          </v-card>
        </v-row>
      </div>
    </div>
    <div class="models-wrapper hidden-sm-and-up">
      <div id="models-mobile" />
      <div class="models inner-section">
        <span class="models-header mobile-h2 ml-3">модельный ряд</span>
           <v-slide-group
      v-model="models"
      center-active
      class="pb-4"
    >
      <v-slide-item
        v-slot="{ active, toggle }"
      >
        <v-card
        color="transparent"
          class="ma-4"
          height="450"
          width="248"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
          <div class="models-card-image-wrapper">
              <v-img src="/tt11.jpg" width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table', hash: '#top'}" class="mobile-h3 models-card-link"><span class="mobile-h3 models-card-link">карл четырехногий →</span></nuxt-link>
            <span class="heading-s-regular-mobile"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
        </v-col>
        </v-card>
      </v-slide-item>
      <v-slide-item
        v-slot="{ active, toggle }"
      >
      
        <v-card
        color="transparent"
          class="ma-4"
          height="450"
          width="248"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
          <div class="models-card-image-wrapper">
              <v-img src="/tt2.jpg" width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table1', hash: '#top'}" class="mobile-h3 models-card-link"><span class="mobile-h3 models-card-link">плоский джо →</span></nuxt-link>
            <span class="heading-s-regular-mobile"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
        </v-col>
        </v-card>
      </v-slide-item>
      <v-slide-item
        v-slot="{ toggle }"
      >
        <v-card
          color="transparent"
          class="ma-4"
          height="450"
          width="248"
          elevation="0"
          rounded="0"
          @click="toggle"
        >
        <v-col class="slider-item">
          <div class="models-card-image-wrapper">
              <v-img src="/tt44.jpg" width="100%" height="100%" contain></v-img>
            </div>
            <nuxt-link :to="{path: '/table2', hash: '#top'}" class="mobile-h3 models-card-link"><span class="mobile-h3 models-card-link">дубовый багет →</span></nuxt-link>
            <span class="heading-s-regular-mobile"
              >Интеграл Фурье, следовательно, реально накладывает криволинейный
              интеграл. Нечетная функция естественно привлекает интеграл по
              поверхности.</span
            >
        </v-col>
        </v-card>
      </v-slide-item>
    </v-slide-group>
          <v-card elevation="0" rounded="0" class="models-card">
       
          </v-card>
          <v-card elevation="0" rounded="0" class="models-card">
           
          </v-card>
          <v-card elevation="0" rounded="0" class="models-card">
            
          </v-card>
      </div>
    </div>
    <div class="team-wrapper hidden-sm-and-down">
      <div id="team" />
      <div class="team inner-section">
        <span class="heading-h2">команда</span>
        <span class="heading-m-light-desktop"
          >Сумма ряда, конечно, накладывает неопределенный интеграл, что и
          требовалось доказать. Интеграл Дирихле, следовательно, трансформирует
          полином. Метод последовательных приближений, исключая очевидный
          случай, стабилизирует постулат. Огибающая существенно упорядочивает
          неопровержимый интеграл Пуассона, что и требовалось доказать. Функция
          B(x,y) непосредственно концентрирует лист Мёбиуса</span
        >
        <v-img src="/team.png" />
      </div>
    </div>
    <div class="team-wrapper hidden-sm-and-up">
      <div id="team-mobile" />
      <div class="team  ml-6">
        <span class="mobile-h2">команда</span>
        <span class="heading-m-light-mobile"
          >Сумма ряда, конечно, накладывает неопределенный интеграл, что и
          требовалось доказать. Интеграл Дирихле, следовательно, трансформирует
          полином. Метод последовательных приближений, исключая очевидный
          случай, стабилизирует постулат. Огибающая существенно упорядочивает
          неопровержимый интеграл Пуассона, что и требовалось доказать. Функция
          B(x,y) непосредственно концентрирует лист Мёбиуса</span
        >
        <v-img src="/team.png" height="350px" cover class="team-mobile-image"/>
      </div>
    </div>
    <div class="philosophy">
      <div class="inner-section">
        <span class="heading-h2 philosophy-heading text-sm-center hidden-sm-and-down">наша философия качества</span>
        <span class="mobile-h2 philosophy-heading text-sm-center hidden-sm-and-up">наша философия качества</span>

        <div class="philosophy-wrapper">
        <div class="philosophy-card">
          <v-img src="/ph1.svg" width="82" height="82" contain class="mb-md-4"></v-img>
          <span class="heading-m-light-desktop">Обязательный контроль качества каждого изделия

</span>
        </div>
        <div class="philosophy-card">
          <v-img src="/ph4.svg" width="82" height="82" contain class="mb-md-4"></v-img>
          <span class="heading-m-light-desktop">Гарантия на материалы и качество работ

</span>
        </div>
        <div class="philosophy-card">
          <v-img src="/ph3.svg" width="82" height="82" contain class="mb-md-4"></v-img>
          <span class="heading-m-light-desktop">Длительное тестирование долговечности каждой<br/> модели

</span>
        </div>
        <div class="philosophy-card">
          <v-img src="/ph2.svg" width="82" height="82" contain class="mb-md-4"></v-img>
          <span class="heading-m-light-desktop">Только материалы высших сортов

</span>
        </div>
      </div>
      </div>

    </div>
    <div class="footer-wrapper hidden-sm-and-down">
      
      <div class="footer inner-section">
        <v-row class="justify-space-between footer-row">
          <v-col cols="3"><span class="heading-h2">Контакты</span></v-col>
          <v-col>
            <div class="footer-ur-row">
              <v-col cols="6" class="pa-0">
                <span class="text-xs-regular">Юрлицо</span>
                <p class="ur-name">ООО «Деревянные Братья»</p>
              </v-col>
              <v-col cols="4" class="pa-0">
                <span class="text-xs-regular">Телефон</span>
                <p class="ur-name">+7 911 987 87 87</p>
              </v-col>
              <div id="contacts" />
              <v-col cols="3" class="align-center justify-center d-flex pa-0">
                <v-row class="justify-center">
                  <v-btn class="mr-6" color="white" fab width="48" height="48"><svg width="20" height="16" viewBox="0 0 20 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0 6.12V11.75C0 12.7446 0.395088 13.6984 1.09835 14.4017C1.80161 15.1049 2.75544 15.5 3.75 15.5H16.25C17.2446 15.5 18.1984 15.1049 18.9017 14.4017C19.6049 13.6984 20 12.7446 20 11.75V6.12L10.5125 10.39C10.3514 10.4624 10.1767 10.4999 10 10.4999C9.82332 10.4999 9.64865 10.4624 9.4875 10.39L0 6.12ZM0.0924999 3.42L10 7.88L19.9075 3.42C19.7193 2.59069 19.2548 1.84998 18.5902 1.3194C17.9256 0.78882 17.1004 0.499885 16.25 0.5H3.75C2.8996 0.499885 2.07441 0.78882 1.40982 1.3194C0.745234 1.84998 0.280723 2.59069 0.0924999 3.42Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                  <v-btn class="mr-6" fab width="48" height="48"><svg width="22" height="18" viewBox="0 0 22 18" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M20.1743 0.221969L1.38428 7.46771C0.101941 7.98277 0.10936 8.69812 1.14901 9.01712L5.97315 10.522L17.1348 3.47975C17.6626 3.15863 18.1448 3.33138 17.7484 3.68322L8.70527 11.8446H8.70315L8.70527 11.8457L8.3725 16.8182C8.86 16.8182 9.07513 16.5946 9.34856 16.3307L11.6917 14.0522L16.5657 17.6522C17.4644 18.1472 18.1098 17.8928 18.3334 16.8203L21.5329 1.7417C21.8604 0.428627 21.0316 -0.165912 20.1743 0.221969Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                  <v-btn fab width="48" height="48"><svg width="23" height="22" viewBox="0 0 23 22" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M20.3777 5.08737C17.0777 -0.000168176 10.3402 -1.51268 5.11513 1.64984C0.0275903 4.81237 -1.62242 11.6874 1.6776 16.775L1.95261 17.1875L0.852597 21.3125L4.97763 20.2125L5.39013 20.4875C7.17765 21.45 9.10266 22 11.0277 22C13.0902 22 15.1527 21.45 16.9402 20.35C22.0278 17.05 23.5403 10.3124 20.3777 5.08737ZM17.4902 15.675C16.9402 16.5 16.2527 17.05 15.2902 17.1875C14.7402 17.1875 14.0527 17.4625 11.3027 16.3625C8.96516 15.2624 7.04014 13.4749 5.66513 11.4124C4.84013 10.4499 4.42762 9.2124 4.29012 7.97489C4.29012 6.87489 4.70263 5.91238 5.39013 5.22487C5.66513 4.94987 5.94014 4.81237 6.21514 4.81237H6.90264C7.17765 4.81237 7.45265 4.81237 7.59015 5.36237C7.86515 6.04988 8.55266 7.69989 8.55266 7.83739C8.69016 7.97489 8.69016 8.2499 8.55266 8.3874C8.69016 8.6624 8.55266 8.9374 8.41516 9.0749C8.27765 9.2124 8.14015 9.4874 8.00265 9.62491C7.72765 9.76241 7.59015 10.0374 7.72765 10.3124C8.27765 11.1374 8.96516 11.9624 9.65266 12.6499C10.4777 13.3374 11.3027 13.8874 12.2652 14.2999C12.5402 14.4374 12.8152 14.4374 12.9527 14.1624C13.0902 13.8874 13.7777 13.1999 14.0527 12.9249C14.3277 12.6499 14.4652 12.6499 14.7402 12.7874L16.9402 13.8874C17.2152 14.0249 17.4902 14.1624 17.6277 14.2999C17.7652 14.7124 17.7652 15.2624 17.4902 15.675Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                </v-row>
              </v-col>
            </div>
            <v-row class="ma-0">
            <span class="text-xs-regular" style="color: #373737">Авторские права на дизайн и конструкцию мебели, а также на все материалы представленные на сайте, защищены. Использование контента третьими лицами, в том числе копирование, распространение, воспроизведение в любой форме - возможны только с письменного разрешения ООО «Деревянные Братья» ©</span>
          </v-row>
          <span class="text-xs-regular mt-4" style="color: #8d8d8d">© 2022 Flatwood</span>
          </v-col>

        </v-row>

      </div>
    </div>

    <div class="footer-wrapper-mobile hidden-sm-and-up">
      <div id="contacts-mobile" />
      <div class="footer-mobile inner-section-mobile">
        <v-col class="justify-space-between footer-row pt-10">
          <v-col cols="3"><span class="heading-h2 mb-5">Контакты</span></v-col>
          <v-col>
            <div class="footer-ur-row">
              <v-col cols="12" class="pa-0">
                <span class="text-xs-regular">Юрлицо</span>
                <p class="ur-name">ООО «Деревянные Братья»</p>
              </v-col>
              <v-col cols="12" class="pa-0 mt-4">
                <span class="text-xs-regular">Телефон</span>
                <p class="ur-name">+7 911 987 87 87</p>
              </v-col>
              <v-col cols="12" class="align-center justify-center d-flex pa-0 px-0 mt-4 mb-4">
                <v-col class="justify-center pa-0">
                  <v-btn class="mr-6" color="white" fab width="48" height="48"><svg width="20" height="16" viewBox="0 0 20 16" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M0 6.12V11.75C0 12.7446 0.395088 13.6984 1.09835 14.4017C1.80161 15.1049 2.75544 15.5 3.75 15.5H16.25C17.2446 15.5 18.1984 15.1049 18.9017 14.4017C19.6049 13.6984 20 12.7446 20 11.75V6.12L10.5125 10.39C10.3514 10.4624 10.1767 10.4999 10 10.4999C9.82332 10.4999 9.64865 10.4624 9.4875 10.39L0 6.12ZM0.0924999 3.42L10 7.88L19.9075 3.42C19.7193 2.59069 19.2548 1.84998 18.5902 1.3194C17.9256 0.78882 17.1004 0.499885 16.25 0.5H3.75C2.8996 0.499885 2.07441 0.78882 1.40982 1.3194C0.745234 1.84998 0.280723 2.59069 0.0924999 3.42Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                  <v-btn class="mr-6" fab width="48" height="48"><svg width="22" height="18" viewBox="0 0 22 18" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M20.1743 0.221969L1.38428 7.46771C0.101941 7.98277 0.10936 8.69812 1.14901 9.01712L5.97315 10.522L17.1348 3.47975C17.6626 3.15863 18.1448 3.33138 17.7484 3.68322L8.70527 11.8446H8.70315L8.70527 11.8457L8.3725 16.8182C8.86 16.8182 9.07513 16.5946 9.34856 16.3307L11.6917 14.0522L16.5657 17.6522C17.4644 18.1472 18.1098 17.8928 18.3334 16.8203L21.5329 1.7417C21.8604 0.428627 21.0316 -0.165912 20.1743 0.221969Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                  <v-btn fab width="48" height="48"><svg width="23" height="22" viewBox="0 0 23 22" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M20.3777 5.08737C17.0777 -0.000168176 10.3402 -1.51268 5.11513 1.64984C0.0275903 4.81237 -1.62242 11.6874 1.6776 16.775L1.95261 17.1875L0.852597 21.3125L4.97763 20.2125L5.39013 20.4875C7.17765 21.45 9.10266 22 11.0277 22C13.0902 22 15.1527 21.45 16.9402 20.35C22.0278 17.05 23.5403 10.3124 20.3777 5.08737ZM17.4902 15.675C16.9402 16.5 16.2527 17.05 15.2902 17.1875C14.7402 17.1875 14.0527 17.4625 11.3027 16.3625C8.96516 15.2624 7.04014 13.4749 5.66513 11.4124C4.84013 10.4499 4.42762 9.2124 4.29012 7.97489C4.29012 6.87489 4.70263 5.91238 5.39013 5.22487C5.66513 4.94987 5.94014 4.81237 6.21514 4.81237H6.90264C7.17765 4.81237 7.45265 4.81237 7.59015 5.36237C7.86515 6.04988 8.55266 7.69989 8.55266 7.83739C8.69016 7.97489 8.69016 8.2499 8.55266 8.3874C8.69016 8.6624 8.55266 8.9374 8.41516 9.0749C8.27765 9.2124 8.14015 9.4874 8.00265 9.62491C7.72765 9.76241 7.59015 10.0374 7.72765 10.3124C8.27765 11.1374 8.96516 11.9624 9.65266 12.6499C10.4777 13.3374 11.3027 13.8874 12.2652 14.2999C12.5402 14.4374 12.8152 14.4374 12.9527 14.1624C13.0902 13.8874 13.7777 13.1999 14.0527 12.9249C14.3277 12.6499 14.4652 12.6499 14.7402 12.7874L16.9402 13.8874C17.2152 14.0249 17.4902 14.1624 17.6277 14.2999C17.7652 14.7124 17.7652 15.2624 17.4902 15.675Z" fill="#DB8E5A"/>
</svg>
</v-btn>
                </v-col>
              </v-col>
            </div>
            <v-row class="ma-0">
            <span class="text-xs-regular mt-4 mb-4" style="color: #373737 !important;">Авторские права на дизайн и конструкцию мебели, а также на все материалы представленные на сайте, защищены. Использование контента третьими лицами, в том числе копирование, распространение, воспроизведение в любой форме - возможны только с письменного разрешения ООО «Деревянные Братья» ©</span>
          </v-row>
          <span class="text-xs-regular mt-4" style="color: #8d8d8d">© 2022 Flatwood</span>
          </v-col>

        </v-col>
      </div>
    </div>
      <v-btn fab fixed @click="handleScroll" elevation="1" class="scroll-to-top"><v-icon class="scroll-to-top-icon">mdi-chevron-up</v-icon></v-btn>
          <v-dialog persistent fullscreen content-class="mobile-menu-container" v-model="menuVisible">
      <ul class="menu-mobele-list">
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#production-mobile'}" class="menu-mobile-item-text" >производство</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#models-mobile'}" class="menu-mobile-item-text" >модельный ряд</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#team-mobile'}" class="menu-mobile-item-text" >команда</nuxt-link></li>
            <li class="menu-mobile-item-text" @click="menuVisible=false"><nuxt-link :to="{path: '/', hash: '#contacts-mobile'}" class="menu-mobile-item-text" >Контакты</nuxt-link></li>
          </ul>
          <v-fab rounded="10" class="mobile-menu-close-button" @click="menuVisible=false">
            <v-icon class="mobile-menu-close-button" large style="color: #000 !important">mdi-close</v-icon>
          </v-fab>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      menuVisible: false,
      model: 0,
      models: 0
    }
  },
  methods: {
    handleScroll() {
      console.log(this.$route.fullPath);
      console.log();
      if (this.$route.fullPath.includes('#')) {
        this.$router.push(this.$route.path.split('#'))
        return
      }
      
      this.$router.push('/#top')
    },
  },
};
</script>



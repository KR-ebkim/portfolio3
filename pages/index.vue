<script setup>
import { ref } from 'vue'
import { useDisplay } from 'vuetify'
import SlideImage1 from "@/assets/main/main_bg01.jpg"
import SlideImage2 from "@/assets/main/main_bg02.jpg"
import SlideImage3 from "@/assets/main/main_bg03.jpg"
import SlideImage4 from "@/assets/main/main_bg04.jpg"
import SlideImage5 from "@/assets/main/main_bg05.jpg"
import SlideImage6 from "@/assets/main/main_bg06.jpg"
import msR from "@/assets/main/main_sportsbook.png"
import ms2 from "@/assets/main/main_livecaisno.png"
import ms3 from "@/assets/main/main_slots.png"
import ms4 from "@/assets/main/main_esports.png"
import ms5 from "@/assets/main/main_premiumgames.png"
import ms6 from "@/assets/main/main_packages.png"


const email = ref("");
const password = ref("");
const { mdAndUp } = useDisplay()

const { ruleEmail, rulePassLen, ruleRequired } = useFormRules();

const submit = async () => { };
const slide = ref([
  {
    src: SlideImage1,
  },
  {
    src: SlideImage2,
  },
  {
    src: SlideImage3,
  },
  {
    src: SlideImage4,
  },
  {
    src: SlideImage5,
  },
  {
    src: SlideImage6,
  },
]);
</script>

<template>
   
  <v-card class="rounded-0" flat style="font-family:titleGothic1">
    <Swiper :modules="[SwiperAutoplay, SwiperPagination, SwiperMousewheel, SwiperEffectFade]" :slides-per-view="1"
      :loop="true" :pagination="true" :mousewheel="true" :autoplay="{delay: 7000, disableOnInteraction: false}"  :effect="'fade'"
       
      >
      

      <!-- 1번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage1" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
                <v-card class="textGroup1" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#A755FF;">SPORTS BOOK</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#스포츠북<br>그 이상 차별화된
                      솔루션!</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Beyond Technology</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle" >최고의 베팅게임
                      소프트웨어 솔루션 제공업체,<br>
                      풍부한 경험과 기술로 최고의 고객 맞춤<br class="mo"> 서비스를 제공합니다.</span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/products/sportsBook">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn><!--color: #231815;-->
                </v-card>
                <v-col>
                  <v-img :src="msR" class="msR"></v-img>
                </v-col>
            </v-card>
            <v-card class="SrollDownCircle rounded-circle text-center" width="140px" height="140px" color="white" variant="outlined">
                <v-card-text class="mt-5">Scroll Down</v-card-text>
                <v-icon>mdi-arrow-down</v-icon>
              </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>
    

      <!-- 2번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage2" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
              <v-row>
                <v-card class="textGroup2" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#F015A7;">LIVE CASINO</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#라이브 카지노<br>최고의 게임
                      경험</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Casino Software</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle">
                      당사의 최첨단 제품과 업계 최고의 플랫폼은<br>
                      플레이어에게 가장 확실한 게임 경험을 제공합니다.</span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/products/liveCasino">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn>
                </v-card>
                <v-col>
                  <v-img :src="ms2" class="msL"></v-img>
                </v-col>
              </v-row>
            </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>


      <!-- 3번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage3" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
              <v-row>
                <v-card class="textGroup1" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#1896F5;">SLOTS</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#단일 통합<br>모든 슬롯게임 제공</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Top Slot Providers</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle">
                    단일 통합으로 최고의 게임 제공업체의 모든 슬롯 게임.<br>
                    #60개 이상 최고의 슬롯 제공업체<br class="mo"> #빠른 실행 #단일 통합 API #모바일 호환성</span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/products/slots">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn><!--color: #231815;-->
                </v-card>
                <v-col>
                  <v-img :src="ms3" class="msR"></v-img>
                </v-col>
              </v-row>
            </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>


      <!-- 4번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage4" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
              <v-row>
                <v-card class="textGroup2" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#F015A7;">E-SPORTS</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#E-스포츠<br>데이터 피드 API</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Data Feed API</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle">
                      매월 수천 개의 E-스포츠 이벤트 및<br class="mo"> 대회에 대한 액세스를 제공합니다.<br>
                      배당률, 일정, 통계, 점수, 정산 등을 다루는<br class="mo"> E스포츠 데이터 API입니다.</span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/products/eSports">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn>
                </v-card>
                <v-col>
                  <v-img :src="ms4" class="msL"></v-img>
                </v-col>
              </v-row>
            </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>


      <!-- 5번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage5" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
              <v-row>
                <v-card class="textGroup1" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#A755FF;">PREMIUM GAMES</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#프리미엄 게임<br>
                  더 좋은 조건으로!</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Better Terms</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle" >
                      같은 게임이라도 조금 더 좋은 조건으로!<br>
                      여러가지로 비교하고 사용해주세요. </span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/products/premiumGames">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn><!--color: #231815;-->
                </v-card>
                <v-col>
                  <v-img :src="ms5" class="msR"></v-img>
                </v-col>
              </v-row>
            </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>


      <!-- 6번 슬라이드 -->
      <SwiperSlide>
        <v-card class="BG rounded-0" flat>
          <v-img :src="SlideImage6" height="100%" cover>
            <v-card class="Slide" height="100%" color="transparent" flat>
              <v-row>
                <v-card class="textGroup2" width="100%" color="transparent" flat>
                  <span class="category" style="font-weight: 700; color:#1896F5;">PACKAGES</span>
                  <v-sheet class="title" height="215" color="transparent"><span class="title">#패키지 기본형,<br>실속형, 맞춤형</span></v-sheet>
                  <v-sheet class="tag" color="transparent"><span class="tag">#Basic #Economy<br class="mo"> #Customized</span></v-sheet>
                  <v-sheet class="subtitle" color="transparent"><span class="subtitle">
                      패키지 결정에 어려움이 있으신가요?<br class="mo"> 실시간 상담을 통해 해결해보세요!<br>
                      사이트 운영 및 관리 노하우를<br class="mo"> 24/7 언제든지 상담해드립니다.</span></v-sheet>
                  <v-btn width="145px" height="50px" style="font-size: 15px; padding-left: 20px; color: white;"
                    color="#7300F0" variant="outlined" to="/packages/pricing">자세히 보기<v-icon class="ml-1" size="25px">mdi-arrow-right</v-icon></v-btn>
                </v-card>
                <v-col>
                  <v-img :src="ms6" class="msL"></v-img>
                </v-col>
              </v-row>
            </v-card>
          </v-img>
        </v-card>
      </SwiperSlide>
    </Swiper>
  </v-card>
</template>



<style>
.mo{
  display: block;
}

.swiper-pagination {
  top: 50%;
  margin-top: 50%;
  transform: rotate(90deg);
  transform-origin: right center;
}

.swiper-pagination-bullet {
  background-color: rgba(255, 255, 255, 0.8);
  padding: 6px;
}

.swiper-pagination-bullet-active {
  background-color: white;
}

.msR {
  width: 300px;
  height: 325px;
  position: absolute;
  top: 2%;
  left: 50%;
  margin-left: -140px;
}

.msL {
  width: 300px;
  height: 275px;
  position: absolute;
  top: 5%;
  left: 50%;
  margin-left: -130px;
}

.BG {
  height: 100%;
  position: relative;
}

.category {
  font-size: 15px;
  font-family: 'SBAggroB';
}

.textGroup1 {
  text-align: center;
  width: 100%;
  margin: 370px auto;
}

.textGroup2 {
  text-align: center;
  width: 100%;
  margin: 360px auto;
}

.title {
  margin-top: 10px;
  margin-bottom: 50px;
  font-size: 30px;
  color: white;
  font-family: 'SBAggroB';
}

.tag {
  font-size: 20px;
  color: white;
  margin-top: -115px;
  margin-bottom: 20px;
  font-family: 'SBAggroB';
}

.subtitle {
  font-weight: 100;
  font-size: 15px;
  color: rgba(255, 255, 255, 0.6);
  margin: 0 auto 45px auto;
  padding: 30px;
}

.subtitle span{
  padding: 0;
}

.SrollDownCircle{
  display: none;
}

@media screen and (min-width: 768px) {
  .mo{
    display: none;
  }

  .BG {
    height: 100%;
  }

  .textGroup1 {
    margin-top: 500px;
    margin-left: 3%;
  }

  .textGroup2 {
    margin-top: 500px;
    margin-left: 3%;
  }

  .category {
    font-size: 30px;
    margin-bottom: 60px;
  }

  .title {
    font-size: 55px;
    margin-bottom: 75px;
  }

  .tag {
    font-size: 35px;
  }

  .subtitle {
    width: 650px;
    font-size: 20px;
    margin-bottom: 45px;
    font-weight: 100;
    padding: 0px;
  }

  .msR {
    width: 400px;
    height: 450px;
    position: absolute;
    top: 2%;
    left: 50%;
    margin-left: -200px;
  }

  .msL {
    width: 400px;
    height: 450px;
    position: absolute;
    top: 2%;
    left: 50%;
    margin-left: -200px;
  }
}

@media screen and (min-width: 1280px) {
  .mo{
    display: none;
  }

  .BG {
    height: calc(100vh - 60px);
  }

  .Slide{
    top:50%;
    margin-top: -350px;
  }

  .SrollDownCircle{
    position: absolute;
    bottom: 5%;
    left: 50%;
    margin-left: -50px;
    display: block;
  }

  .category {
    font-size: 15px;
  }

  .textGroup1 {
    text-align: start;
    top: 0%;
    left: 50%;
    margin: 4% 0 0 -630px;
  }

  .textGroup2 {
    text-align: start;
    top: 0;
    left: 50%;
    margin: 5% 0 0 100px;
  }

  .title {
    line-height: 80px;
    margin-top: 25px;
    font-size: 65px;
  }

  .tag {
    font-size: 25px;
    margin-top: -110px;
    margin-bottom: 80px;
  }

  .subtitle {
    width: 650px;
    font-weight: 100;
    font-size: 15px;
    margin: -20px 0 45px 0;
  }

  .msR {
    width: 635px;
    height: 650px;
    top: 0;
    left: 50%;
    margin:0;
  }

  .msL {
    width: 635px;
    height: 650px;
    top: 0;
    left: 50%;
    margin:0 0 0 -630px;
  }
}
</style>

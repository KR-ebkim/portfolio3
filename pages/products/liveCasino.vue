<script setup>
import { ref } from 'vue'
import SubLiveCasinoImg from '@/assets/images/sub_livecasino_img02.png'
import Card1 from '@/assets/images/dragon_tiger.png'
import Card2 from '@/assets/images/live_baccarat.png'
import Card3 from '@/assets/images/live_blackjack.png'
import Card4 from '@/assets/images/live_poker.png'
import Card5 from '@/assets/images/live_roulette.png'
import { useDisplay } from 'vuetify'

const { mdAndUp } = useDisplay()

const list = ref([{
  image: Card1,
  text: "라이브 용호",
  eng: 'Dragon Tiger'
},
{
  image: Card2,
  text: "라이브 바카라",
  eng: 'Live Baccarat'
},
{
  image: Card3,
  text: "라이브 블랙잭",
  eng: 'Live Blackjack'
},
{
  image: Card4,
  text: "라이브 포커",
  eng: 'Live Poker'
},
{
  image: Card5,
  text: "라이브 룰렛",
  eng: 'Live Roulette'
},
])
const model = ref()

</script>
<template>
  <v-card color="#141414" flat rounded="0">
    <v-card class="BG1 rounded-0" width="100%" color="#141414" flat>
      <v-img :src="SubLiveCasinoImg" class="IMG" style="margin-top: 80px;"></v-img>
      <v-card class="LogoGroup rounded-0" color="rgba(24,24,24,0.5)" flat>
        <v-row no-gutters>
          <v-col>
            <v-img class="logo1"></v-img>
          </v-col>
          <v-col>
            <v-img class="logo2"></v-img>
          </v-col>
        </v-row>

        <v-row no-gutters>
          <v-col>
            <v-img class="logo3"></v-img>
          </v-col>
          <v-col>
            <v-img class="logo4"></v-img>
          </v-col>
          <v-col>
            <v-img class="logo5"></v-img>
          </v-col>
        </v-row>

        <v-row no-gutters>
          <v-col>
            <v-img class="logo6"></v-img>
          </v-col>
          <v-col>
            <v-img class="logo7"></v-img>
          </v-col>
          <v-col>
            <!--로고 추가 가능-->
          </v-col>
          <v-col>
            <!--로고 추가 가능-->
          </v-col>
          <v-col>
            <!--로고 추가 가능-->
          </v-col>
        </v-row>
      </v-card>
    </v-card>






    <div class="CardBG">
      <h1 style="font-size: 40px;" class="text-white ml-16 mb-10">Premium Casino</h1>

      <Swiper :modules="[SwiperVirtual]" :slides-per-view="mdAndUp ? 3 : 1" :virtual="true" :space-between="90">
        <SwiperSlide v-for="item in list" :key="item.text">
          <v-card class=" rounded-xl text-white" max-width="535"  flat color="transparent">
            <v-img :src="item.image" cover eager=""></v-img>


            <v-card-title class="cardTitle">{{ item.text }}</v-card-title>
            <v-card-subtitle class="cardSubtitle">{{ item.eng }}</v-card-subtitle>
          </v-card>
        </SwiperSlide>
      </Swiper>

    </div>

  </v-card>




</template>
  

  
  
<style>
.BG1 {
  position: relative;
  height: 900px;
}

.IMG {
  margin: 20px;
  height: 100%;
}

.LogoGroup {
  position: absolute;
  top: 0;
  left: 50%;
  width: 350px;
  height: 850px;
  margin: 25px 0 0 -177px;
}

.logo1 {
  background-image: url(@/assets/images/logo_evolutiongaming_on.png);
  background-position: center;
  background-size: 250px;
  margin: 20px 0 20px 0;
  width: 350px;
  height: 100px;
}

.logo2 {
  background-image: url(@/assets/images/logo_ezugi_on.png);
  background-position: center;
  background-size: 200px;
  margin-bottom: 20px;
  width: 350px;
  height: 100px;
}

.logo3 {
  background-image: url(@/assets/images/logo_netent_on.png);
  background-position: center;
  background-size: 165px;
  margin-bottom: 30px;
  width: 350px;
  height: 100px;
}

.logo4 {
  background-image: url(@/assets/images/logo_pragmatic_on.png);
  background-position: center;
  background-size: 200px;
  width: 350px;
  height: 100px;
}

.logo5 {
  background-image: url(@/assets/images/logo_microgaming_on.png);
  background-position: center;
  background-size: 200px;
  width: 350px;
  height: 150px;
}

.logo6 {
  background-image: url(@/assets/images/logo_habanero_on.png);
  background-position: center;
  background-size: 200px;
  width: 350px;
  height: 100px;
}

.logo7 {
  background-image: url(@/assets/images/logo_sexygaming_on.png);
  background-position: center;
  background-size: 150px;
  width: 350px;
  height: 100px;
}

.BG2 {
  padding: 155px 0px 190px 0px;
}

.Slides {
  margin-left: 16.5%;
}

.SlideList {
  margin-left: -50px;
}

.cardText {
  margin: 20px 0px 0px -15px;
}

.cardTitle {
  font-size: 25px;
}

.cardSubtitle {
  font-size: 15px;
}

.CardBG{
  background-color:black;
  padding: 25% 7px 25% 2%;
}

@media screen and (min-width: 768px) {

  .BG1 {
    height: 575px;
  }

  .IMG {
    height: 400px;
  }

  .LogoGroup {
    position: absolute;
    width: 700px;
    height: 400px;
    margin: 85px 0 0 -350px;
  }

  .logo1 {
    background-size: 250px;
    margin-top: 20px;
  }

  .logo2 {
    background-size: 200px;
    margin-top: 20px;
  }

  .logo3 {
    background-size: 135px;
    width: auto;
  }

  .logo4 {
    background-size: 175px;
    width: auto;
  }

  .logo5 {
    background-size: 175px;
    width: auto;
    margin-top: -20px;
  }

  .logo6 {
    margin-left: 20px;
    background-size: 120px;
    width: auto;
  }

  .logo7 {
    background-size: 100px;
    width: auto;
  }

  .CardBG{
  background-color:black;
  padding: 100px 7px 100px 17.5%;
}

}

@media screen and (min-width: 1280px) {
  .BG1 {
    height: 800px;
  }

  .LogoGroup {
    width: 1280px;
    height: 625px;
    margin: 85px 0 0 -640px;
  }

  .IMG {
    height: 600px;
  }


  .logo1 {
    background-image: url(@/assets/images/logo_evolutiongaming_off.png);
    background-size: 365px;
    height: 250px;
    margin: 0;
    width: auto;
  }

  .logo1:hover {
    background-image: url(@/assets/images/logo_evolutiongaming_on.png);
    background-size: 365px;
    width: auto;
  }

  .logo2 {
    background-image: url(@/assets/images/logo_ezugi_off.png);
    background-size: 300px;
    height: 250px;
    width: auto;
  }

  .logo2:hover {
    background-image: url(@/assets/images/logo_ezugi_on.png);
    background-size: 300px;
    width: auto;
  }

  .logo3 {
    background-image: url(@/assets/images/logo_netent_off.png);
    background-size: 165px;
    height: 150px;
    width: auto;
  }

  .logo3:hover {
    background-image: url(@/assets/images/logo_netent_on.png);
    background-size: 165px;
    width: auto;
  }

  .logo4 {
    background-image: url(@/assets/images/logo_pragmatic_off.png);
    background-size: 225px;
    height: 160px;
    width: auto;
  }

  .logo4:hover {
    background-image: url(@/assets/images/logo_pragmatic_on.png);
    background-size: 225px;
    width: auto;
  }

  .logo5 {
    background-image: url(@/assets/images/logo_microgaming_off.png);
    background-size: 275px;
    height: 180px;
    width: auto;
  }

  .logo5:hover {
    background-image: url(@/assets/images/logo_microgaming_on.png);
    background-size: 275px;
    width: auto;
  }

  .logo6 {
    margin: 0;
    background-image: url(@/assets/images/logo_habanero_off.png);
    background-position-x: 50px;
    background-size: 190px;
    height: 115px;
    width: auto;
  }

  .logo6:hover {
    margin: 0;
    background-image: url(@/assets/images/logo_habanero_on.png);
    background-position-x: 50px;
    background-size: 190px;
    width: auto;
  }

  .logo7 {
    margin: 0;
    background-image: url(@/assets/images/logo_sexygaming_off.png);
    background-position-x: 50px;
    background-size: 150px;
    height: 115px;
    width: auto;
  }

  .logo7:hover {
    margin: 0;
    background-image: url(@/assets/images/logo_sexygaming_on.png);
    background-position-x: 50px;
    background-size: 150px;
    width: auto;
  }

  .CardBG{
  background-color:black;
  padding: 150px 7px 150px 2%;
}

}
</style>
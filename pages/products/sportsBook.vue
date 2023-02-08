<script setup>
import { ref } from "vue"
import { useDisplay } from 'vuetify'
import sub_sportsbook_img02 from "@/assets/images/sub_sportsbook_img02.png"

const { mdAndUp } = useDisplay()
const list = ref([
  { icon: "iconfont icon-yundongchang", title: "Pre-Match", content: "매월 140,000+ 경기 프리매치 피드<br>서비스를 제공합니다." },
  { icon: "iconfont icon-live4", title: "Live Feed", content: "매월 50,000+ 경기 실시간 피드<br>서비스를 제공합니다." },
  { icon: "iconfont icon-activity-s", title: "All Matches", content: "비인기 종목부터 탑티어 경기들<br>전부 제공합니다." },
  { icon: "iconfont icon-icon_guanlianzhanghu", title: "Traker", content: "H2H, STAT CENTRE 및 매치 트래커<br>서비스를 제공합니다." },
  { icon: "iconfont icon-zhuzhuangtu", title: "Risk Management", content: "리스크 매니지먼트<br>서비스를 제공합니다." },
  { icon: "iconfont icon-shoujidiannao", title: "High Quality", content: "고품질 모바일 및 PC 스포츠북 기능을<br>제공합니다." },
  { icon: "iconfont icon-zizhukaitongmoniqiquanzhanghu01", title: "Convenience", content: "최고성을 자랑하는 편리한 관리자 기능을<br>제공합니다." },
  { icon: "iconfont icon-kefu15", title: "Service Center", content: "24/7 서포트 지원<br>서비스를 제공합니다." },
  { icon: "iconfont icon-hehuorenzhaomu", title: "", content: "더좋은 서비스 제공을 위해서<br>힘쓰겠습니다." },

])
</script>
  

<template>
  <v-card class="rounded-0" color="#141414">
    <v-img cover :src="sub_sportsbook_img02" max-width="1000" class="mx-auto my-10 align-center">
      <v-row justify="center">
        <v-col v-for="item in list" :key="item" :cols="mdAndUp ? '4' : 'auto'">
          <v-card width="270px" height="300px" class="py-5" color="transparent" flat > 
            <v-card elevation="10" width="115" height="115" class="IconCardList mx-auto d-flex align-center justify-center" color="black" rounded="xl" >
              
              <span class="CardIcons" :class="item.icon" style="padding: 50px; font-size: 55px; font-weight: 100;"></span>
            </v-card>
            <v-card-title class="text-center text-white" style="font-weight: 600">
              {{ item.title }}
            </v-card-title>
            <v-card-text v-html="item.content" class="text-center text-grey" style="font-weight: 600;">
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-img>
  </v-card>
</template>


<style>
.IconCardList{
  box-shadow: 0px 10px 30px rgb(255 255 255 / 25%) !important;
  -webkit-box-shadow: 0px 10px 30px rgb(255 255 255 / 25%) !important;
  margin-bottom: 35px;
}

.IconCardList:hover{
  box-shadow: 0px 10px 30px rgb(167 85 255 / 50%) !important;
  -webkit-box-shadow: 0px 10px 30px rgb(167 85 255 / 50%) !important;
}

.CardIcons:hover{
  color: #A755FF;
}

</style>

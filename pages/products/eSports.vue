<script setup>
import { ref } from "vue"
import { useDisplay } from 'vuetify'
import sub_esports_img02 from "@/assets/images/sub_esports_img02.png"
import sub_sportsbook_img02 from "@/assets/images/sub_esports_img02.png"

const { mdAndUp } = useDisplay()
const list = ref([
  { icon: "iconfont icon-yundongchang", title: "Pre-Match", content: "매월 5,000+ 경기 프리매치 피드<br>서비스를 제공합니다." },
  { icon: "iconfont icon-live4", title: "Live Feed", content: "매월 12,000+ 경기 실시간 피드<br>서비스를 제공합니다." },
  { icon: "iconfont icon-activity-s", title: "Championship", content: "12+ 메이저 챔피언쉽 피드 경기들<br>전부 제공합니다." },
  { icon: "iconfont icon-hd", title: "HD", content: "HD 퀄리티 스트리밍<br>서비스를 제공합니다." },
  { icon: "iconfont icon-zhuzhuangtu", title: "Risk Management", content: "리스크 매니지먼트<br>서비스를 제공합니다." },
  { icon: "iconfont icon-youxitianchong", title: "Bet Type", content: "최고의 E-SPORTS 베팅 타입들<br>제공합니다." },

])
</script>
  

<template>
  <v-card class="py-11" color="#141414" rounded="0" flat>
    <v-img cover :src="sub_esports_img02" max-width="1000" class="mx-auto align-center">
      <v-row justify="center">
        <v-col v-for="item in list" :key="item" :cols="mdAndUp ? '4' : 'auto'">
          <v-card width="270px" height="300px" color="transparent" style="padding-top:20px; padding-bottom:100px;" flat > 
            <v-card elevation="10" width="115" height="115" class="IconCardList mx-auto d-flex align-center justify-center" color="black" rounded="xl" >
              
              <span class="CardIcons" :class="item.icon" style="padding: 50px; font-size: 55px; font-weight: 100;"></span>
            </v-card>
            <v-card-title class="text-center text-white" style="font-weight:600">
              {{ item.title }}
            </v-card-title>
            <v-card-text v-html="item.content" class="text-center text-grey" style="font-weight:600">
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-img>
  </v-card>
</template>
  

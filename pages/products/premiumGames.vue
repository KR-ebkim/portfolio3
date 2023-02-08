<script setup>
import { ref } from "vue"
import { useDisplay } from 'vuetify'
import premiumgames_img01 from "@/assets/images/premiumgames_img01.png"
import premiumgames_img02 from "@/assets/images/premiumgames_img02.png"
import premiumgames_img03 from "@/assets/images/premiumgames_img03.png"
import premiumgames_img04 from "@/assets/images/premiumgames_img04.png"
import premiumgames_img05 from "@/assets/images/premiumgames_img05.png"
import premiumgames_img06 from "@/assets/images/premiumgames_img06.png"
import premiumgames_img07 from "@/assets/images/premiumgames_img07.png"
import premiumgames_img08 from "@/assets/images/premiumgames_img08.png"
import premiumgames_img09 from "@/assets/images/premiumgames_img09.png"
import premiumgames_img10 from "@/assets/images/premiumgames_img10.png"
import premiumgames_img11 from "@/assets/images/premiumgames_img11.png"
import premiumgames_img12 from "@/assets/images/premiumgames_img12.png"
import premiumgames_img13 from "@/assets/images/premiumgames_img13.png"
import premiumgames_img14 from "@/assets/images/premiumgames_img14.png"
import premiumgames_img15 from "@/assets/images/premiumgames_img15.png"

const { mdAndUp } = useDisplay()
const list = ref([
  { image: premiumgames_img01,  content: "EOS 파월볼 제공" },
  { image: premiumgames_img02,  content: "파워사다리 제공" },
  { image: premiumgames_img03,  content: "스피드 홈런 제공" },
  { image: premiumgames_img04,  content: "FX 마진 게임 제공" },
  { image: premiumgames_img05,  content: "스카이파크 게임 제공" },
  { image: premiumgames_img06,  content: "BET365 가상 축구 게임 제공" },
  { image: premiumgames_img07,  content: "BET365 가상 농구 게임 제공" },
  { image: premiumgames_img08,  content: "BET365 가상 미식축구 게임 제공" },
  { image: premiumgames_img09,  content: "BET365 가상 테니스 게임 제공" },
  { image: premiumgames_img10,  content: "BET365 가상 크리켓 게임 제공" },
  { image: premiumgames_img11,  content: "BET365 가상 트로팅 게임 제공" },
  { image: premiumgames_img12,  content: "BET365 가상 사이클링 게임 제공" },
  { image: premiumgames_img13,  content: "BET365 가상 다트 게임 제공" },
  { image: premiumgames_img14,  content: "BET365 가상 경마 게임 제공" },
  { image: premiumgames_img15,  content: "BET365 가상 개경주 게임 제공" },

])
</script>
  

<template>
  <v-card color="#141414" rounded="0" flat>
    <v-card rounded="0" flat color="transparent" max-width="900" class="mx-auto my-16"> 
      <v-row justify="center">
        <v-col v-for="item in list" :key="item" :cols="mdAndUp ? '4' : 'auto'">
        
            <v-card  width="270" class="mx-auto pt-4 px-4" color="black" rounded="xl">
              <v-img cover :src="item.image"  class="mx-auto align-center">
              </v-img>          
              <v-card-text class="text-center">
                {{ item.content }}
              </v-card-text>
            </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-card>
</template>
  

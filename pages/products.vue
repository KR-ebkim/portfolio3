
<script setup>
import { ref } from 'vue'
import sub_sportsbook_img01 from "@/assets/images/sub_sportsbook_img01.jpg"
import sub_esports_img01 from "@/assets/images/sub_esports_img01.jpg"
import sub_slots_img01 from "@/assets/images/sub_slots_img01.png"
import sub_livecasino_img01 from "@/assets/images/sub_livecasino_img01.jpg"
import sub_premiumgames_img01 from "@/assets/images/sub_premiumgames_img01.jpg"


const links = ref([
    { text: 'Sports Book', to: "/products/sportsBook", bg: sub_sportsbook_img01, subTitle: '고품격 스포츠북 서비스를 소개 합니다.' },
    { text: 'E-Sports', to: "/products/eSports", bg: sub_esports_img01, subTitle: "월드 클래스 E-SPORTS 서비스를 소개 합니다." },
    { text: 'Slots', to: "/products/slots", bg: sub_slots_img01, subTitle: "빛나는 슬롯 게임들을 소개 합니다. " },
    { text: 'Live Casino', to: "/products/liveCasino", bg: sub_livecasino_img01, subTitle: "최고의 종합 카지노 서비스를 소개 합니다." },
    { text: 'Premium Games', to: "/products/premiumGames", bg: sub_premiumgames_img01, subTitle: "차별화된 게임 서비스를 소개 합니다." },
])
const tab = ref(0)
const componentKey = ref(0)
</script>

<template>
    <v-card flat rounded="0">
        <v-img :src="links[tab].bg" cover class="d-flex align-center">
                <v-card :style="mdAndUp ? '' : 'padding: 50px'" color="transparent" flat height="100%">
                    <v-card-text class="ResTitle text-white text-center" style="font-family: 'SBAggroB'; line-height: 40px">
                        {{ links[tab].text }}
                    </v-card-text>
                    <v-card-text class="ResSub text-white text-center" style="font-family:titleGothic1;">
                        <div class="ResSub" style="font-family:titleGothic3;">
                        {{ links[tab].subTitle }}
                    </div>
                    </v-card-text>
                </v-card>
        </v-img>
    </v-card>
    <div class="d-flex align-center justify-center" width="100%" style="background-color: black; height: 85px;">
        <v-tabs v-model="tab" bg-color="black" color="grey" height="85px">
            <v-tab v-for="item in links" :key="item.text" :to="item.to" class="mx-6" style="font-size: 15px; text-transform:none !important;"
                >
                {{ item.text }}</v-tab>
        </v-tabs>

    </div>
    <NuxtPage></NuxtPage>
</template>


<style>
@media screen and (max-width: 767px) {
    .ResTitle{
        font-size: 24px;
        line-height: 70px;
    }

	.ResSub{
		font-size: 14px;
		line-height: 25px;
	}
}

@media screen and (min-width: 768px) {
    .ResTitle{
        margin-bottom: 35px;
        font-size: 40px;
    }

	.ResSub{
		font-size: 30px;
		line-height: 70px;
	}
}
</style>
<script setup>
import { ref } from 'vue'
import sub_packages_img01 from "@/assets/images/sub_packages_img01.jpg"


const links = ref([
	{ Title: 'Packages', tab: 'Pricing', to: "/packages/pricing", bg: sub_packages_img01, subTitle: '패키지 A/B 서비스' },
])
const tab = ref(0)
const componentKey = ref(0)
const email = ref("");
const password = ref("");

const { ruleEmail, rulePassLen, ruleRequired } = useFormRules();

const submit = async () => { };

const service1 = ref([
	{ text: '프리매치 피드' },
	{ text: 'E-Sports 피드' },
	{ text: '버추얼 게임' },
	{ text: '미니 게임' },
	{ text: '가상 게임' },
	{ text: '인플레이 피드' },
]);

const service2 = ref([
	{ text: '※초기 셋팅비용 및 서버비용' },
	{ text: '셋팅비용: 20,000,000 원', more: ' (1회성)' },
	{ text: '서버비용: 4,000,000 원' },
	{ text2: '카지노 종량제 (선불): 10%' }
])

const service3 = ref([
	{ textA: '서버비용: 4,000,000 원' },
	{ textA: '스포츠 GGR (월 배팅-당첨 % 요율)' },
	{ moreA1: '카지노 GGR (월 배팅-당첨 10% 고정 요율)' },
	{ moreA2: '(패키지 B의 경우 별도로 선불 카지노 알구매비용 10%를 지불)' },
	{ textB: '프리매치+인플레이', moreB1: '(월 30,000 경기 이상 제공, 요율은 배팅 금액 - 당첨금액으로 계산됩니다.)' },
	{ textB: '500,000,000 원 이하 ~ 8%' },
	{ textB: '500,000,000 원 - 150,000,000 원 ~ 7%' },
	{ textB: '150,000,000 원 - 300,000,000 원 ~ 6%' },
	{ textB: '300,000,000 원 이상 ~ 5%' },
	{ moreB2: '</br> 카지노 고정 10% (요율은 배팅 금액 - 당첨금액으로 계산됩니다)' }
])

const service4 = ref([
	{ text: '신규 계약 시 최소한의 자본금은 200,000,000 원 이상 잔고가 확인되어야 솔루션 임대가 가능합니다.' },
])
</script>



<template>
	<v-card class="rounded-0">
		<v-img :src="links[tab].bg" cover class="d-flex align-center">
			<v-card class="py-15" color="transparent" flat height="100%">
				<v-card-text class="ResTitle text-white text-center" style="font-family: 'SBAggroB';">
					{{ links[tab].Title }}
				</v-card-text>
				<v-card-text class="ResSub text-white text-center" style="font-family:titleGothic1;">
					{{ links[tab].subTitle }}를 소개 합니다.
				</v-card-text>
			</v-card>
		</v-img>
	</v-card>
	<div class="d-flex align-center justify-center" width="100%" style="background-color: black; height: 85px;">
		<v-tabs v-model="tab" bg-color="black" color="grey" height="85px">
			<v-tab v-for="item in links" :key="item.text" :to="item.to"
				style="font-size: 15px; text-transform:none !important;">
				{{ item.tab }}</v-tab>
		</v-tabs>
	</div>
	<v-sheet class="BG" color="#141414">

		<!--모바일-->
		<v-container class="BOX mo">
			<div style="margin: 50px 0 150px 0">
				<v-card class="text-center py-10" style="font-family: 'SBAggroB'" color="black" flat>Packages A
					<v-card-title
						style="font-family: 'SBAggroB';font-size: 25px; color: #A755FF;">24,000,000원</v-card-title></v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">서비스 종목</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div class="my-3">
						<v-card-text style="color: white;">
							<v-card-text class="textAble" v-for="item in service1" :key="item">{{ item.text }}
								<v-icon size="25px" style="margin-left:3px; margin-bottom:2px"
									color="green">mdi-check</v-icon>
							</v-card-text>
							<v-card-text class="textDisable">슬롯 게임<v-icon
									class="iconDisable">mdi-window-close</v-icon></v-card-text>
							<v-card-text class="textDisable">라이브 카지노<v-icon
									class="iconDisable">mdi-window-close</v-icon></v-card-text>
						</v-card-text>
					</div>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">초기 비용</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div style="color: white;" class="my-3">
						<v-card-text class="text-center pa-1" v-for="item in service2" :key="item"
							style="font-size: 15px;">
							{{ item.text }}
							<span style="color:#51EF64">{{ item.more }}</span>
						</v-card-text>
						<v-card class="d-flex justify-space-between ma-5" style="background-color: #121212;">
							<v-card-text style="font-size: 15px; color:#AFAFAF">총합계:</v-card-text>
							<v-card-text style="font-size: 16px; color:white">24,000,000 원</v-card-text>
						</v-card>
					</div>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">월 임대지출 비용</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div class="ThirdCard py-5">
						<v-card-text class="py-0 px-10 my-2" style="color:white; font-size: 15px;"
							v-for="item in service3" :key="item">
							{{ item.textA }}
						</v-card-text>
					</div>
					<v-card-text style="color:white; font-size:15px" class="py-0 px-5 mt-2 mb-5"
						v-for="item in service3" :key="item">
						{{ item.textB }}
						<span style="font-size: 12px">
							{{ item.moreB1 }}
						</span>
					</v-card-text>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">임대조건</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<v-card-text class="TAtext3 py-0 px-5" style="margin: 2% 10% 0% 14%; color: white;"
						v-for="item in service4" :key="item">
						{{ item.text }}
					</v-card-text>
					<v-card-text class="TAtext3 pt-1 px-5" style="color: #F54F51; font-weight: 700; margin-top: -10px;"
						v-for="item in service4" :key="item">
						{{ item.more }}
					</v-card-text>
				</v-card>
			</div>

			<div>
				<v-card class="text-center py-10" style="font-family: 'SBAggroB'" color="black" flat>Packages B
					<v-card-title
						style="font-family: 'SBAggroB';font-size: 25px; color: #A755FF;">24,000,000원
					</v-card-title>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">서비스 종목</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div class="my-3 py-5" style="color:white">
						<v-card-text class="textAble" v-for="item in service1" :key="item">{{ item.text }}<v-icon
								size="25px" style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
						<v-card-text class="textAble">슬롯 게임<v-icon size="25px"
								style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
						<v-card-text class="textAble">라이브 카지노<v-icon size="25px"
								style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
					</div>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">초기 비용</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div style="color: white;" class="my-3">
						<v-card-text class="text-center pa-1" v-for="item in service2" :key="item"
							style="font-size: 15px;">
							{{ item.text }}
							<span style="color:#51EF64">{{ item.more }}</span>
							{{ item.text2 }}
						</v-card-text>

						<v-card class="d-flex justify-space-between ma-5" style="background-color: #121212;">
							<v-card-text style="font-size: 13px; color:#AFAFAF">총합계:</v-card-text>
							<v-card-text style="font-size: 13px; color:white">24,000,000 원 + 카지노 종량제 10%</v-card-text>
						</v-card>
					</div>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">월 임대지출 비용</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<div class="ThirdCard py-5" style="color:white">
						<v-card-text class="pt-2 pb-0 TAtext2" v-for="item in service3" :key="item">
								{{ item.textA }}
								{{ item.moreA1 }}
								<span style="font-size:12px;">
									{{ item.moreA2 }}
								</span>
							</v-card-text>
						<v-card-text class="TAtext2 px-5 pb-1 pt-0" v-for="item in service3" :key="item">
							{{ item.textB }}
							<span style="font-size: 12px">
								{{ item.moreB1 }}
							</span>

						</v-card-text>
						<v-card-text class="TAtext2 px-5 py-0" v-for="item in service3" :key="item" v-html="item.moreB2">				
						</v-card-text>						
					</div>
				</v-card>

				<v-card class="my-2 text-center" style="color: #A755FF; background-color: black;" flat>
					<v-card-title class="my-1" style="font-weight: 700;">임대조건</v-card-title>
					<v-divider style="background-color: #A755FF;"></v-divider>
					<v-card-text class="TAtext3 py-0 px-5" style="margin: 2% 10% 0% 14%; color: white;"
						v-for="item in service4" :key="item">
						{{ item.text }}
					</v-card-text>
					<v-card-text class="TAtext3 pt-1 px-5" style="color: #F54F51; font-weight: 700; margin-top: -10px;"
						v-for="item in service4" :key="item">
						{{ item.more }}
					</v-card-text>
				</v-card>
			</div>
		</v-container>





		<!--타블렛-->
		<v-container class="BOX ta">
			<v-row no-gutters>
				<v-col cols="2"><v-card class="rounded-lg List1 ma-2" color="black"></v-card></v-col>
				<v-col><v-card class="rounded-lg List1 pt-10 ma-2 text-center" color="black">Packages A<v-card-title
							style="font-family: 'SBAggroB'; font-size: 25px; color: #A755FF;">24,000,000원</v-card-title></v-card></v-col>
				<v-col><v-card class="rounded-lg List1 pt-8 ma-2 text-center" color="black">Packages B<v-card-title
							style="font-family: 'SBAggroB'; font-size: 25px; color: #A755FF;">24,000,000원<br><span
								style="font-size:13px">+ 카지노 종량제 10%</span></v-card-title></v-card></v-col>
			</v-row>

			<v-row no-gutters>
				<v-col cols="2"><v-card class="rounded-lg List2 ma-2 d-flex align-center justify-center text-center"
						style=" font-size: 15px; font-weight: 600; color: #A755FF; background-color: black;">서비스<br>종목</v-card></v-col>
				<v-col><v-card class="rounded-lg List2 text-center ma-2" style="padding-top: 27px" color="black">
						<v-card-text class="textAble" v-for="item in service1" :key="item">{{ item.text }}<v-icon
								size="25px" style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
						<v-card-text class="textDisable">슬롯 게임<v-icon
								class="iconDisable">mdi-window-close</v-icon></v-card-text>
						<v-card-text class="textDisable">라이브 카지노<v-icon
								class="iconDisable">mdi-window-close</v-icon></v-card-text>
					</v-card></v-col>
				<v-col>
					<v-card class="rounded-lg List2 text-center ma-2" style="padding-top: 27px" color="black">
						<v-card-text class="textAble" v-for="item in service1" :key="item">{{ item.text }}<v-icon
								size="25px" style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
						<v-card-text class="textAble">슬롯 게임<v-icon size="25px"
								style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
						<v-card-text class="textAble">라이브 카지노<v-icon size="25px"
								style="margin-left:3px; margin-bottom:2px"
								color="green">mdi-check</v-icon></v-card-text>
					</v-card>

				</v-col>

			</v-row>

			<v-row no-gutters>
				<v-col cols="2">
					<v-card class="rounded-lg List3 ma-2 d-flex align-center justify-center text-center"
						style=" font-size: 15px; font-weight: 600; color: #A755FF; background-color: black;">초기비용</v-card>
				</v-col>
				<v-col><v-card class="rounded-lg List3 pa-10 ma-2" color="black">
						<v-card-text class="text-center pa-1" v-for="item in service2" :key="item"
							style="font-size: 15px;">
							{{ item.text }}
							<span style="color:#51EF64">{{ item.more }}</span>
						</v-card-text>
						<v-divider class="mt-9" style="background-color: #2E2E2E;"></v-divider>
						<div class="d-flex justify-space-between">
							<span class="pt-3" style="color:#AFAFAF">총합계:</span>
							<span class="pt-3">24,000,000 원</span>
						</div>
					</v-card></v-col>
				<v-col><v-card class="rounded-lg List3 pa-6 ma-2" color="black">
						<v-card-text class="text-center pa-1" v-for="item in service2" :key="item"
							style="font-size: 15px;">
							{{ item.text }}
							<span style="color:#51EF64">{{ item.more }}</span>
							{{ item.text2 }}
						</v-card-text>
						<v-divider class="mt-8" style="background-color: #2E2E2E;"></v-divider>
						<div class="d-flex justify-space-between">
							<span class="pt-3" style="color:#AFAFAF">총합계:</span>
							<span class="pt-3">24,000,000 원 + 카지노 종량제 10%</span>
						</div>
					</v-card></v-col>
			</v-row>

			<v-row no-gutters>
				<v-col cols="2"><v-card class="rounded-lg List4 ma-2 d-flex align-center justify-center text-center"
						style=" font-size: 15px; font-weight: 600; color: #A755FF; background-color: black;">월 임대지출<br>
						비용</v-card></v-col>
				<v-col>
					<v-card class="TAtext rounded-lg List4 ma-2 text-center" color="black">
						<div class="ThirdCard">
							<v-card-text class="pa-0 my-2" style="font-size: 15px;" v-for="item in service3"
								:key="item">
								{{ item.textA }}
							</v-card-text>
						</div>
						<v-card-text style="font-size:15px" class="pa-0 my-2" v-for="item in service3" :key="item">
							{{ item.textB }}
							<span style="font-size: 12px">
								{{ item.moreB1 }}
							</span>
						</v-card-text>
					</v-card>
				</v-col>
				<v-col> <v-card class="TAtext2 rounded-lg List4 ma-2 text-center" color="black">
						<div style="margin-top: 5%; margin-bottom: 5%; ">
							<v-card-text class="pa-0 TAtext2" v-for="item in service3" :key="item">
								{{ item.textA }}
								{{ item.moreA1 }}
								<span style="font-size:12px;">
									{{ item.moreA2 }}
								</span>
							</v-card-text>

						</div>
						<v-card-text class="TAtext2 pa-0" v-for="item in service3" :key="item">
							{{ item.textB }}
							<span style="font-size: 12px">
								{{ item.moreB1 }}
							</span>

						</v-card-text>
						<v-card-text class="TAtext2 pa-0" v-for="item in service3" :key="item" v-html="item.moreB2">						
						</v-card-text>
					</v-card></v-col>
			</v-row>

			<v-row no-gutters>
				<v-col cols="2"><v-card class="rounded-lg List5 ma-2 d-flex align-center justify-center text-center"
						style="height: 100px; font-size: 15px; font-weight: 600; color: #A755FF; background-color: black;">임대조건
					</v-card></v-col>
				<v-col>
					<v-card class="LastCard rounded-lg List5 ma-2 text-center" height="100px" color="black"><v-card-text
							style="margin: 2% 10% 0% 14%;" class="TAtext3 py-0 px-5" v-for="item in service4"
							:key="item">
							{{ item.text }}
						</v-card-text>
						<v-card-text class="TAtext3 pt-1 px-5"
							style="color: #F54F51; font-weight: 700; margin-top: -10px;" v-for="item in service4"
							:key="item">
							{{ item.more }}
						</v-card-text>
					</v-card>
				</v-col>
				<v-col>
					<v-card class="LastCard rounded-lg List5 ma-2 text-center" height="100px" color="black"><v-card-text
							style="margin: 2% 10% 0 14%;" class="TAtext3 
						py-0 px-5" v-for="item in service4" :key="item">
							{{ item.text }}
						</v-card-text>
						<v-card-text class="TAtext3 pt-1 px-5"
							style="color: #F54F51; font-weight: 700; margin-top: -10px;" v-for="item in service4"
							:key="item">
							{{ item.more }}
						</v-card-text>
					</v-card>
				</v-col>
			</v-row>
			<div class="d-flex justify-center mt-10">
				<v-btn width="250" height="50" variant="outlined" color="white" style="font-size:15px;">패키지 A/B 구매하기
					<v-icon class="ml-1" size="30px">mdi-arrow-right</v-icon></v-btn>
			</div>
		</v-container>

	</v-sheet>


</template>




<style scoped>
.mo {
	display: block;
}

.ta {
	display: none;
}

.BG {
	height: 100%;
}

.List1 {
	height: 150px;
	font-family: 'SBAggroB';
	font-size: 15px;
}

.List2 {
	height: 300px;
}

.List3 {
	height: 240px;
}

.List4 {
	height: 375px;
}

.List5 {
	height: 125px;
}

.textAble {
	margin: -25px 0;
}

.textDisable {
	margin: -21px 0;
	color: gray;
	text-decoration: line-through;
}

.iconDisable {
	margin-left: 3px;
	margin-bottom: 2px;
	color: red;
}

@media screen and (max-width: 767px) {

	.ResTitle {
		font-size: 25px;
	}

	.ResSub {
		font-size: 15px;
		line-height: 25px;
	}
}

@media screen and (min-width: 768px) {
	.mo {
		display: none;
	}

	.ta {
		display: block;
	}

	.BOX {
		padding: 3% 1%;
	}

	.ThirdCard {
		margin-bottom: 20%;
	}

	.LastCard {
		padding-top: 3%;
	}

	.TAtext {
		padding: 10% 5%;
		margin-bottom: 5px;
	}

	.TAtext2 {
		padding: 5%;
		font-size: 12px;
		margin-bottom: 5px;
	}

	.TAtext3 {
		font-size: 12px;
	}

	.ResTitle {
		font-size: 40px;

	}

	.ResSub {
		font-size: 30px;
		line-height: 45px;
	}
}

@media screen and (min-width: 1280px) {

	.BG {
		height: 1515px;
	}

	.BOX {
		padding: 3% 10%;
	}

	.ThirdCard {
		margin-top: -11px;
		margin-bottom: 14%;
	}

	.LastCard {
		padding-top: 3%;
	}

	.TAtext {
		padding: 10% 5%;
		margin-bottom: 5px;
	}

	.TAtext2 {
		padding: 5%;
		font-size: 15px;
		margin-bottom: 5px;
	}

	.TAtext3 {
		font-size: 15px;
	}


}
</style>
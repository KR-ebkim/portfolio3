<script setup>
import CompanyImage from '@/assets/images/company_img01.jpg'
import CompanyLogo from '@/assets/images/company_logo.png'
import ontactBg from '@/assets/common/contact_bg.jpg'
import { useDisplay } from 'vuetify'

const { mdAndUp } = useDisplay()
const email = ref("");
const password = ref("");

const { ruleEmail, rulePassLen, ruleRequired } = useFormRules();

const submit = async () => { };
</script>


<template>
	<v-sheet color="black">

		<v-card color="black" class="py-16">
			<v-card max-width="800" class="mx-auto " flat color="transparent">
				<v-card-text style="font-size:20px; line-height:24px">업계에서 가장 정확하고 뛰어난 종합 북메이커 서비스를 제공해드리고
					있습니다.</v-card-text>
				<v-card-text style="font-size:14px; line-height:18px" class="pt-0 text-grey">Our company provides the most
					accurate and comprehensive bookmaker service in the industry.
				</v-card-text>
			</v-card>
		</v-card>

		<v-sheet color="#181818" style="margin-bottom: 120px;">

			<v-card max-width="1280" color="transparent" flat class="mx-auto py-16">
				<v-row justify="center" class="px-3">
					<v-col>
						<v-card class="card1 cardLabel text-center rounded-xl" height="230"
							color="black">
							<v-card-text class="cardText"><span
									class="iconfont icon-shejiyishu text-grey-darken-4 ml-5" style="font-weight:100"></span>#혁신적인 디자인</v-card-text>
						</v-card>
					</v-col>
					<v-col>
						<v-card class="card2 cardLabel text-center rounded-xl" height="230"
							color="black">
							<v-card-text class="cardText" style="margin-top:88px;"><span
									class="iconfont iconfont2 icon-kaifajichushezhi text-grey-darken-4" style="font-size: 53px; font-weight:100; margin-right: 25px; margin-top: 0px;" ></span>#기술</v-card-text>
						</v-card>
					</v-col>
					<v-col>
						<v-card class="card3 cardLabel text-center rounded-xl" height="230" 
							color="black">
							<v-card-text class="cardText" ><span
									class="iconfont icon-liujisuan text-grey-darken-4 ml-5" style="font-weight:100"></span>#초고속 배당
								업데이트</v-card-text>
						</v-card>
					</v-col>
				</v-row>
				<v-row justify="center" class="px-3">
					<v-col :cols="mdAndUp ? '4' : ''">
						<v-card class="card4 cardLabel text-center rounded-xl" height="230"
							color="black">
							<v-card-text class="cardText"><span
									class="iconfont icon-icon-mianxing_fuzhi_gaoxingjiabi text-grey-darken-4 ml-5" style="font-size: 75px; font-weight:100; margin-right: 0px;"></span>#가격
								대비 최고의 가치</v-card-text>
						</v-card>
					</v-col>
					<v-col :cols="mdAndUp ? '8' : ''">
						<v-card class="card5 cardLabel text-center rounded-xl" height="230"
							color="black">
							<v-card-text class="cardText"><span
									class="iconfont icon-kefu17 text-grey-darken-4 ml-5" style="font-weight:100;"></span>#초고속 배당
								업데이트</v-card-text>
						</v-card>
					</v-col>
				</v-row>
			</v-card>




		</v-sheet>

		<v-card class="text-center" color="black" style="padding-bottom: 110px;">
			<span
				:style="mdAndUp ? 'font-size: 60px; margin-bottom: 70px; font-weight: 700;' : 'font-size: 40px; margin-bottom: 70px; font-weight: 700;'" style="font-family: 'SBAggroB'">
				Our Mission
			</span>

			<v-card-text class="text-center" style="font-size: 20px; line-height: 30px;">
				저렴한 비용 대비 최고의 품질 제공,<br>
				혁신적인 플랫폼 기능,<br>
				헌신적인 고객서비스 및 파트너분들이 모두 만족할수 있는<br>
				<span style="color: #A755FF;">최상의 원스톱 플랫폼 서비스를 제공</span>해드리는게 저희의 사명입니다.
			</v-card-text>

			<v-card-text style="font-size: 20px; line-height: 30px;">
				가장 정확하고, 가장 뛰어난 원스톱 플랫폼 숍이 될수있게 나날이 발전하는 플랫폼 서비스를 제공하겠습니다.
			</v-card-text>
		</v-card>

	</v-sheet>

</template>



<style scoped>
.m1 {
	display: grid;
	place-items: center;
}


.cardLabel {
	margin-right: 25px;
	color: aliceblue;
}

.cardText {
	margin-top: 5.5rem;
	font-size: 22px;
	font-weight: 700;
	display: flex;
	justify-content: center;
	text-align: center;
}

.cardLabel:last-child {
	margin: 0px;
}

.iconfont {
	color: rgb(35, 24, 21);
	font-size: 60px;
	margin-right: 20px;
}

.iconfont2 {
	color: rgb(137, 137, 137);
}

.card1:hover {
	background-image: url(@/assets/images/company_bgimg01.png);
}

.card2:hover {
	background-image: url(@/assets/images/company_bgimg02.png);
}

.card3:hover {
	background-image: url(@/assets/images/company_bgimg03.png);
}

.card4:hover {
	background-image: url(@/assets/images/company_bgimg04.png);
}

.card5:hover {
	background-image: url(@/assets/images/company_bgimg05.png);
}

@media screen and (max-width: 299px) {

	.iconfont{
		margin-top: 10px;
	}
	.cardText{
		margin-right: 10px;
		margin-top: 75px;
		line-height: 30px;
	}
	
}

@media screen and (min-width: 300px) {

	.cardLabel{
		min-width: 300px;
		margin-top: 50px;
	}
}

</style>

<script setup>
import { ref } from 'vue'
import { useDisplay } from 'vuetify'
import bgImage from '~/assets/common/contact_bg.jpg'
import logo from '~/assets/common/logo.png'


const route = useRoute()
console.log(route.path)
const { mdAndUp } = useDisplay()
const drawer = ref(false)
const links1 = ref([
	{
		name: "Products", child: [
			{ name: "Sports book", to: "/products/sportsBook", type: "child" },
			{ name: "E-sports", to: "/products/eSports", type: "child" },
			{ name: "Slots", to: "/products/slots", type: "child" },
			{ name: "Live Casino", to: "/products/liveCasino", type: "child" },
			{ name: "Premium Games", to: "/products/premiumGames", type: "child" },
		]
	},
	{
		name: "Packages", child: [
			{ name: "Pricing", to: "/packages/pricing", type: "child" },
		]
	},

])
const links2 = ref([

	{
		name: "Company", child: [
			{ name: "Introduction", to: "/company/introduction", type: "child" },
		]
	},
	{
		name: "Integrations", child: [
			{ name: "Q&A", to: "", type: "child" },
		]
	},
	{
		name: "Contact", child: [
			{ name: "Sales", to: "", type: "child" },
			{ name: "General", to: "", type: "child" },
		]
	},
])

const SNS = ref([
	{ icon: "iconfont icon-facebook", link:"" },
	{ icon: "iconfont icon-twitter1", link:"" },
	{ icon: "iconfont icon-instagram-fill", link:"" },
	{ icon: "iconfont icon-youtube", link:"" },
	{ icon: "iconfont icon-bxl-telegram", link: "https://t.me/cs_247" },
])

const checkRoute = (value) => {
	let tempValue = false
	value.child.forEach(value => {
		if (route.path == value.to) {
			tempValue = true
		}
	})
	return tempValue
}
</script>


<template>
	<v-app style="font-family:titleGothic1" >
		<v-app-bar color="black" height="60" >

			<v-spacer></v-spacer>
			
			<v-btn id="LangKR" size="lg"><v-icon class="mr-1" color="white">mdi-earth</v-icon>KR</v-btn>
			
			<v-app-bar-nav-icon :rounded="0" variant="text" @click.stop="drawer = !drawer" width="70px" height="100%" color="white" style="margin-right: 0px; background-color:#7300F0;"><v-icon class="DrawerIcon" size="35px">mdi-menu</v-icon></v-app-bar-nav-icon>
		</v-app-bar>
		<v-navigation-drawer v-model="drawer" temporary color="black" style="height:100%; width:100%;" location="right">
			<v-card style="position:relative; overflow-y: scroll;" width="100%" height="100%" color="transparent">
				<div class="SNSbtn">
					<v-btn v-for="item in SNS" :key="item" class="mr-4 mb-2 rounded-circle" width="50" height="50"
						variant="outlined" icon :href="item.link"><span :class="item.icon"
							style="font-size:25px; font-weight: 100;"></span></v-btn>
				</div>

				<v-card :max-width="mdAndUp ? '50%' : '90%'" class="ml-auto" color="transparent" flat>
					<v-row>
						<v-col>
							<v-card v-for="item in links1" :key="item.name" color="transparent" class="mt-10" style="margin-bottom:75px;">
								<v-divider v-if="checkRoute(item)" color="#7300F1" class="pb-3"
									style="width:220px; position:absolute; z-index: 0; top:20px; left:10px"></v-divider>
								<v-btn class="btn mb-2" variant="text">
									<span class="fontstyle mb-5" style="display: block;"
										:style="mdAndUp ? 'font-size: 30px;' : 'font-size: 25px;'">{{ item.name }}</span>
								</v-btn>


								<div v-for="childItem in item.child" :key="childItem.name">
									<v-card class="menuBTN ml-1" :to="childItem.to" @click="drawer = false"
										variant="text" color="white" width="180px" height="40px"
										style="padding: 10px 0 5px 10px" flat>
										<div class="fontstyle mb-5" style="text-transform: unset !important"
											:style="childItem.to == route.path ? 'color:#A755FF;' : ''">
											{{ childItem.name }}
										</div>
									</v-card>
								</div>
							</v-card>
						</v-col>
						<v-col>
							<v-card v-for="item in links2" :key="item.name" color="transparent" class="mt-10" style="margin-bottom: 75px">
								<v-divider v-if="checkRoute(item)" color="#7300F1" class="pb-3"
									style="width:220px; position:absolute; z-index: 0; top:20px; left:10px"></v-divider>
								<v-btn class="btn mb-2" variant="text">
									<span class="fontstyle" style="display: block;"
										:style="mdAndUp ? 'font-size: 30px;' : 'font-size: 25px;'">{{ item.name }}</span>
								</v-btn>
								<div v-for="childItem in item.child" :key="childItem.name">
									<v-card class="menuBTN ml-1" :to="childItem.to" @click="drawer = false"
										variant="text" color="white" width="180px" height="40px"
										style="padding: 10px 0 5px 10px" flat>
										<div class="fontstyle" style="text-transform: unset !important;"
											:style="childItem.to == route.path ? 'color:#A755FF;' : ''">
											{{ childItem.name }}
										</div>
									</v-card>
								</div>
							</v-card>
						</v-col>
					</v-row>
				</v-card>
			</v-card>
		</v-navigation-drawer>
		<v-main>
			<NuxtPage />
		</v-main>
		<v-footer class="pa-0 align-start" flat color="#0C0C0C" v-if="route.path !== '/'">
			<v-card width="100%" color="transparent" rounded="0">
				<v-img :src="bgImage" alt="" max-width="100%" cover class="d-flex align-center">
					<v-card flat color="transparent" class="text-white  mx-auto" max-width="1280" style="padding:2%">
						<v-row justify="center">
							<v-col class="d-flex justify-center align-center" :cols="mdAndUp ? 'auto' : ''">
								<span class="iconfont icon-luntan"
									:style="mdAndUp ? 'font-size: 100px;' : 'width: 10px; font-size: 80px; margin:50px 0 0 -30%;'"></span>
							</v-col>
							<v-col class="d-flex align-center" :cols="mdAndUp ? 'auto' : ''">
								<v-card :style="mdAndUp ? '' : 'width: 215px; margin-left: 20px'"  flat color="transparent">
									<v-card-title class="mb-2 mt-5" style="font-size: 30px;">CONTACT</v-card-title>
									<v-card-text class="mb-2" style="font-size: 18px;">비즈니스 개발팀을 <br class="mo"> 만나보세요</v-card-text>
									<v-card-text
										style="font-size: 13px; color: rgba(255, 255, 255, 0.5); margin-top: -20px;">게임과
										관련된
										요구 사항, 비즈니스 또는 기타 모든 사항에 대해 자유롭게 질문하십시오.</v-card-text>
								</v-card>
							</v-col>
							<v-col class="d-flex align-center" :cols="mdAndUp ? 'auto' : ''">
								<v-card width="100%" :class="mdAndUp ? 'd-flex' : 'd-flex pb-5'" color="transparent"
									flat >
									<v-card class="mx-auto" color="transparent" flat>
									<v-btn height="50" class="mx-auto" variant="outlined"
										style="font-size: 15px; margin-bottom: 20px; padding-left: 20px; color: white;" color="#7300F0">지금 바로
										문의<v-icon style="margin-left: 2px; font-size: 25px;">mdi-arrow-right</v-icon></v-btn>
									</v-card>
								</v-card>
							</v-col>
						</v-row>
					</v-card>
				</v-img>
				<v-card max-width="1600" flat color="#0C0C0C" class="mx-auto pa-8">
					<v-row class="pt-10">
						<v-col :cols="mdAndUp ? '3' : 'auto'">
						</v-col>
						<v-col :cols="mdAndUp ? '5' : 'auto'" style="margin-left: 3%; margin-right: 4%;">
							<v-row>
								<v-col v-for="item in links1" :key="item.name">
									<v-card color="transparent" class="mx-1" flat>
										<div style="font-size:15px; color: white;" class="mb-2">{{ item.name }}</div>
										<div v-for="childItem in item.child" :key="childItem.name">
											<v-card :to="childItem.to" @click="drawer = false" variant="text"
												color="white" flat>
												<div class="mb-1" style="text-transform: unset !important; font-size:10px"
													:style="childItem.to == route.path ? 'color:#A755FF' : ''">
													{{ childItem.name }}
												</div>
											</v-card>
										</div>
									</v-card>
								</v-col>
								<v-col v-for="item in links2" :key="item.name">
									<v-card color="transparent" class="mx-1" flat>
										<div class="mb-2" style="font-size:15px; color: white">{{ item.name }}</div>
										<div v-for="childItem in item.child" :key="childItem.name">
											<v-card :to="childItem.to" @click="drawer = false" variant="text"
												color="white" flat>
												<div class="mb-1" style="text-transform: unset !important; font-size:10px"
													:style="childItem.to == route.path ? 'color:#A755FF' : ''">
													{{ childItem.name }}
												</div>
											</v-card>
										</div>
									</v-card>
								</v-col>
							</v-row>
						</v-col>
						<v-col :cols="mdAndUp ? '3' : 'auto'">
							<v-btn icon variant="outlined" rounded="round" v-for="item in SNS" :key="item" class="ma-2" color="white" :href="item.link">
								<span :class="item.icon" style="font-size:20px; font-weight: 100;"></span>
							</v-btn>


						</v-col>
					</v-row>
				</v-card>
			</v-card>
		</v-footer>
	</v-app>
</template>

<style>

::-webkit-scrollbar {
    display: none;
}

.DrawerIcon{
	-webkit-transform: scaleY(1.2);
    -moz-transform: scaleY(2);
}

.btn {
	text-transform: unset !important;
}

.contact {
	display: grid;
	place-items: center;
}

.fontstyle {
	font-family: 'SBAggroB';
	margin-bottom: 10px;
}

.Drawer{
	overflow: hidden;
}

.menuBTN:hover {
	background-color: rgba(167, 85, 255, 0.5);
	width: 200px;
}


.SNSbtn {
	margin-top: 10%;
	margin-left: 10%;
}

@media screen and (max-width: 280px) {
	#Home{
		margin-left: -10px;
		width: 110px;
	}

	#LangKR{
		margin-right: 3%;
	}
}

@media screen and (min-width: 300px) {
	#Home{
		width: 150px;
	}

	#LangKR{
		margin-right: 5%;
	}
}

@media screen and (min-width: 400px) {
	#Home{
		width: 240px;
		margin-right: 0;
	}

	#LangKR{
		margin-right: 2%;
	}
}

@media screen and (min-width: 420px) {
	#LangKR{
		margin-right: 5%;
	}
}


@media screen and (min-width: 695px) {

	.mo{
		display: none;
	}

	.SNSbtn {
		position: absolute;
		left: 0%;
		bottom: 40%;
	}
}

@media screen and (min-width: 1280px) {

	#LangKR{
		margin-right: 2%;
	}

	.SNSbtn {
		left: -7%;
		bottom: 20%;
	}
}
</style>
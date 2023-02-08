<script setup>
import SubSlotsImg from '@/assets/images/sub_slots_img02.png'

</script>
<template>
  <v-card class="BG rounded-0" width="100%" color="#141414" flat>
    <v-img class="IMG" :src="SubSlotsImg"></v-img>
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
</template>
  

  
  
<style scoped>
.BG {
  position: relative;
  height: 900px;
}

.IMG{
  margin: 20px;
  height: 100%;
}

.LogoGroup{
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
  background-image: url(@/assets/images/logo_habanero_on.png);
  background-position: center;
  background-size: 250px;
  margin-bottom: 20px;
  width: 350px;
  height: 100px;
}

.logo3 {
  background-image: url(@/assets/images/logo_pg_on.png);
  background-position: center;
  background-size: 250px;
  margin-bottom: 30px;
  width: 350px;
  height: 100px;
}

.logo4 {
  background-image: url(@/assets/images/logo_relax_on.png);
  background-position: center;
  background-size: 250px;
  width: 350px;
  height: 100px;
}

.logo5 {
  background-image: url(@/assets/images/logo_pragmatic_on.png);
  background-position: center;
  background-size: 250px;
  width: 350px;
  height: 150px;
}

.logo6 {
  background-image: url(@/assets/images/logo_boongo_on.png);
  background-position: center;
  background-size: 150px;
  width: 350px;
  height: 100px;
}

.logo7 {
  background-image: url(@/assets/images/logo_cq9_on.png);
  background-position: center;
  background-size: 100px;
  width: 350px;
  height: 100px;
}

@media screen and (min-width: 768px) {

  .BG{
    height: 100%;
  }

  .IMG{
    height: 550px;
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
    background-size: 250px;
    margin-top: 20px;
  }

  .logo3 {
    background-size: 200px;
    width: auto;
  }

  .logo4 {
    background-size: 200px;
    width: auto;
  }

  .logo5 {
    background-size: 200px;
    width: auto;
    margin-top: -20px;
  }

  .logo6 {
    margin-left: 30px;
    background-size: 110px;
    width: auto;
  }

  .logo7 {
    margin-left: 10px;
    background-size: 80px;
    width: auto;
  }

}

@media screen and (min-width: 1280px) {
  .BG{
    height: 100vh;
  }

  .LogoGroup {
    width: 1280px;
    height: 630px;
    margin: 150px 0 0 -640px;
  }

  .IMG{
    margin-top: 75px;
    height: 770px;
  }


  .logo1 {
    background-image: url(@/assets/images/logo_evolutiongaming_off.png);
    background-size: 370px;
    height: 250px;
    margin: 0;
    width: auto;
  }

  .logo1:hover {
    background-image: url(@/assets/images/logo_evolutiongaming_on.png);
    background-size: 370px;
    width: auto;
  }

  .logo2 {
    background-image: url(@/assets/images/logo_habanero_off.png);
    background-size: 450px;
    height: 250px;
    width: auto;
  }

  .logo2:hover {
    background-image: url(@/assets/images/logo_habanero_on.png);
    background-size: 450px;
    width: auto;
  }
  .logo3 {
    background-image: url(@/assets/images/logo_pg_off.png);
    background-size: 250px;
    height: 160px;
    width: auto;
  }

  .logo3:hover {
    background-image: url(@/assets/images/logo_pg_on.png);
    background-size: 250px;
    width: auto;
  }

  .logo4 {
    background-image: url(@/assets/images/logo_relax_off.png);
    background-size: 225px;
    height: 160px;
    width: auto;
  }

  .logo4:hover {
    background-image: url(@/assets/images/logo_relax_on.png);
    background-size: 225px;
    width: auto;
  }

  .logo5 {
    background-image: url(@/assets/images/logo_pragmatic_off.png);
    background-size: 230px;
    height: 160px;
    width: auto;
  }

  .logo5:hover {
    background-image: url(@/assets/images/logo_pragmatic_on.png);
    background-size: 230px;
    width: auto;
  }

  .logo6 {
    background-image: url(@/assets/images/logo_boongo_off.png);
    background-position: center;
    background-size: 155px;
    height: 115px;
    width: auto;
  }

  .logo6:hover {
    background-image: url(@/assets/images/logo_boongo_on.png);
    background-position: center;
    background-size: 155px;
    width: auto;
  }

  .logo7 {
    background-image: url(@/assets/images/logo_cq9_off.png);
    background-position: center;
    background-size: 100px;
    height: 115px;
    width: auto;
  }

  .logo7:hover {
    background-image: url(@/assets/images/logo_cq9_on.png);
    background-position: center;
    background-size: 100px;
    width: auto;
  }
}
</style>
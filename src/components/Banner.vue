<template>
  <v-row class="b_container" href="#main">
    <div class="banner">
      <v-img
        src="@/assets/header-iphone.png"
        height="auto"
        max-width="30%"
        centered
        pt-5
      ></v-img>
      <div class="banner_txt">

        <h1>OBOD-ZARBDOR <br />ilovasi</h1>
         <h2 style="color:rgb(43 129 197); font-weight:500">
          MUAMMO UCHUN
        </h2>
        <typewriter
  :speed="200"
  :full-erase="true"
  :interval="300"
  rtl.
  :words='["YECHIM!","TAKLIF!"]'
  style="color:rgb(43 129 197); font-weight:500; font-size:52px; text-align: right">
</typewriter>
        <!-- <h2 style="color:rgb(43 129 197); font-weight:500">
          
        </h2> -->
      </div>
    </div>
  </v-row>
</template>

<script>
export default {
  name: "Banner",
  props: {
    msg: String
  }
};
</script>

<style>
.b_container {
  display: flex;
  align-items: center;
  height: 60vh;
  background-image: linear-gradient(
    to right,
    #19d3dc,
    #18e7d3,
    #18e7d3,
    #19d2dd
  );
  padding: 0;
  margin: 0 auto;
  max-width: 100%;
  background-repeat: no-repeat;
  background-position: center;
}
.banner {
  display: flex;
  max-width: 65%;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  text-align: center;
  margin: 0 auto;
}
.banner_txt h1,
.banner_txt h2 {
  font-size: 54px;
  font-family: "Poppins", sans-serif;
  color: #fff;
  text-align: right;
}
.v-main .row {
  margin: 0;
}
@media (max-width: 959px) {
  .row .b_container {
    height: 40%;
  }
 
  .banner_txt h1,
  .banner_txt h2 {
    font-size: 32px;
  }
}
@media (max-width: 580px) {
.banner {
    flex-direction: column;
    max-width: 100%;
    padding: 7%;
  }
  .v-toolbar__content{
    padding: 0;
  }

}
</style>
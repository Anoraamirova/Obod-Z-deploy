<template>
  <v-row>
    <v-content>
      <v-content-title href="#about">
        <div class="about-block">
          <h3 style="about-title">Ilova haqida</h3>
          <h4 style="font-size: 18px; margin-top: 3%">Obod Zarbdor mobil ilovasi haqida</h4>
          <div class="about-body">
            <div class="about-img">
              <img src="@/assets/header-iphone.png" width="70%" alt="" />
            </div>
            <div class="about-txt">
              <p>
                Muammoni suratga oling! Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating va shu orqali davlatimizdagi nohush xolatlarni oldini oling. Rasmga olingan fotoga izoh qoldiring. Muammo yoki hodisani rasmga oling va izoh qoldiring. Natijalarni kuzatib
                boring Tizim orqali sizning sorovingiz qabul qilingani yoki ishlash jarayonida ekanligi togrisida nazorat o'rnating va shu orqali davlatimizdagi nohush xolatlarni oldini oling
              </p>
            </div>
          </div>
        </div>
      </v-content-title>
    </v-content>
  </v-row>
</template>

<script>
export default {
  name: "About",
  props: {
    msg: String,
  },
};
</script>

<style>
.about-block {
  margin: 5% auto;
}
h3 {
  font-size: 30px;
  text-align: center;
  font-family: "Roboto", sans-serif;
  font-weight: 300;
  color: #232323;
  position: relative;
  padding-bottom: 10px;
  text-transform: uppercase;
}
h3:before {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  height: 2px;
  width: 150px;
  background-color: #19d3dc;
  left: calc(50% - 75px);
}
h3:after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -3px;
  height: 8px;
  width: 8px;
  background-color: #19d3cc;
  left: calc(50% - 4px);
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
}
h4 {
  text-align: center;
  font-family: "Poppins", sans-serif;
  font-weight: 400;
  color: #232323;
  margin-bottom: 30px;
}
.about-body {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  max-width: 70%;
  align-items: center;
}
.about-txt {
  max-width: 50%;
  font-size: 14px;
  color: #666666;
}
</style>

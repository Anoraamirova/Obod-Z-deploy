<template>
  <v-app>
     <v-app-bar class="toolb" fixed app>
      <v-toolbar-title link
        ><v-img
          src="@/assets/obod-zarbdor-logo.svg"
          width="50%"
          centered
        ></v-img
      ></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          flat
          text
          color="white"
          no-borders
          v-for="item in menu"
          :key="item.icon"
          :to="item.link"
          >{{ item.title }}</v-btn
        >
        <v-btn text dark color="rgb(43 129 197)" no-borders
          >Kirish <v-icon right>mdi-login-variant</v-icon>
        </v-btn>
        <v-menu open-on-hover bottom offset-x>
          <template v-slot:activator="{ on, attrs }">
            <v-btn flat text color="rgb(43 129 197)" v-bind="attrs" v-on="on">
              <v-icon>mdi-web</v-icon>
              <v-icon right>mdi-menu-down-outline</v-icon>
            </v-btn>
          </template>

          <v-list color="rgb(43 129 197)">
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
              style="cursor: pointer"
            >
              <v-list-item-title style="color:white">{{
                item.title
              }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-toolbar-items>
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="hidden-md-and-up"
        color="white"
      ></v-app-bar-nav-icon>
    </v-app-bar>
    <v-main>
      <v-navigation-drawer v-model="drawer" absolute left>
        <v-list nav dense>
          <v-list-item-group v-model="group" active-class="cyan lighten-4">
            <v-list-item v-for="item in menu" :key="item.title">
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
       
      <Banner  id="#asosiy"/>
      <About id="about"/>
      <Statistics id="stats" />
      <Features id="features"/>
      <Screenshots id="screens"/>
      <Footer />
    </v-main>
  </v-app>
</template>

<script>

import About from "./components/About";
import Banner from "./components/Banner";
import Features from "./components/Features";
import Statistics from "./components/Statistics";
import Screenshots from "./components/Screenshots";
import Footer from "./components/Footer";

export default {
  
  name: "App",

  components: {
    Banner,
    About,
    Statistics,
    Features,
    Screenshots,
    Footer,
  },

   data() {
    return {
      menu: [
        { icon: "home", title: "Asosiy" },
        { icon: "info", title: "Ilova haqida" },
        { icon: "stat", title: "Statistika" },
        { icon: "features", title: "Afzalliklari" },
        { icon: "instruction", title: "Qollanma" },
      ],
      items: [{ title: "UZB" }, { title: "РУС" }],
      drawer: false,
    };
  },
   methods: {
    menuItems() {
      return this.menu;
    },
  },
};
</script>

<style>
* {
  margin: 0;
}
.toolb {
  padding: 0 5%;
  text-align: center;
  background-image: linear-gradient(to right, #19d3dc, #18e7d3, #18e7d3, #19d2dd);
}
</style>
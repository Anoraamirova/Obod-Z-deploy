<template>
  <v-app ma-0>
    <v-container>
      <v-row href="#afzalliklari">
        <v-col cols="12">
          <h2 class="display-1 text-uppercase text-center font-weight-light h2-decoration">
            Features
          </h2>
          <p class="text-center font-weight-light pa-5">Why this app?</p>
        </v-col>
      </v-row>

      <v-row align="center">
        <v-col cols="12">
          <div class="feature-container">
            <div>
              <div
                v-for="value in features.featuresOne"
                :key="value.index"
                class="item-lists1"
              >
                <p class="text-right font-weight-light">{{ value[0] }}</p>
                <div class="icon-decoration">
                  <v-icon large color="rgba(25, 211, 220,0.9)" class="icons">
                    {{ value[1] }}
                  </v-icon>
                </div>
              </div>
            </div>

            <div class="image-container">
              <img height="75%" width="75%" src="../assets/tel.png" />
            </div>

            <div>
              <div
                v-for="value in features.featuresTwo"
                :key="value.index"
                class="item-lists2"
              >
                <div class="icon-decoration">
                  <v-icon large color="rgba(25, 211, 220,0.9)" class="icons">
                    {{ value[1] }}
                  </v-icon>
                </div>
                <p class="font-weight-light text-left">{{ value[0] }}</p>
              </div>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "Features",
  props: {
    msg: String,
  },

  data() {
    return {
      features: {
        featuresOne: {
          one: ["A quick solution to the problems", "mdi-widgets"],
          two: [
            "Direct communication with officials",
            "mdi-office-building-marker",
          ],
          third: ["Online control over problem solving", "mdi-gavel"],
        },
        featuresTwo: {
          fourth: ["Protect environment", "mdi-tree"],
          fifth: [
            "Convenient system for sending appeals",
            "mdi-email-send-outline",
          ],
          sixth: ["Statistics", "mdi-chart-bar"],
        },
      },
    };
  },
};
</script>

<style scoped>

.h2-decoration{
  position: relative;
  padding-bottom: 10px;
}
.h2-decoration:before {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  height: 2px;
  width: 150px;
  background-color: #19d3dc;
  left: calc(50% - 75px);
}
.h2-decoration:after {
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


.feature-container {
  display: grid;
  grid-template-columns: auto auto auto;
  justify-content: center;
  column-gap: 20px;
  align-items: center;
  /* border: 2px solid black; */
}

.image-container {
  display: flex;
  justify-content: center;
}

.icon-decoration {
  display: inline-block;
  border: rgba(25, 211, 220, 0.9) 2px solid;
  padding: 15px 15px;
  margin-top: 15px;
  margin-bottom: 15px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}

.icons {
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
}

.item-lists1 {
  padding: 20px;
  display: flex;
  align-items: baseline;
  gap: 40px;
  justify-content: flex-end;
}
.item-lists2 {
  padding: 20px;
  display: flex;
  align-items: baseline;
  gap: 40px;
  justify-content: flex-start;
}

@media (min-width: 551px) and (max-width: 1100px) {
  .image-container {
    display: none;
  }
}
@media (max-width: 550px) {
  .feature-container {
    grid-template-columns: auto;
    grid-template-rows: auto auto auto;
  }
}
</style>

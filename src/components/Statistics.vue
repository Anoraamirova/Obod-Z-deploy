<template>
  <div class="statistics" href="#stats">
    <div v-for="(value, name) in datas" :key="name.index" class="p-style">
      <!-- <p>
        <Counter :delay="delay" :endVal="value" :options="options" @ready="onReady" />
      </p>
      -->
      <p>{{ value }}</p>
      <p>{{ name }}</p>
    </div>
  </div>
</template>

<script>
//import Counter from "vue-countup-v2";
export default {
  name: "Statistics",
  props: {
    msg: String,
  },
  components: {
    //  Counter,
  },

  data() {
    return {
      datas: {
        Problems: 76,
        Viewed: 3,
        Solved: 43,
        Rejected: 16,
      },
      delay: 1000,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ",",
        decimal: ".",
        prefix: "",
        suffix: "",
      },
    };
  },
  methods: {
    onReady: function (instance) {
      const that = this;
      instance.update(that.endVal + 100);
    },
  },
};
</script>

<style scoped>
.statistics {
  margin: 0;
  min-height: 400px;
  max-height: 1300px;
  width: 100%;
  display: grid;
  grid-template-columns: auto auto auto auto;
  background: url("../assets/ach-bg-img.jpg") center center/cover no-repeat;
  position: relative;
  align-items: center;
  justify-content: center;
  column-gap: 200px;
}

.statistics:before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(25, 211, 220, 0.9);
}

.p-style {
  font-family: "Poppins", sans-serif;
  text-align: center;
  font-size: 30px;
  color: #fff;
  z-index: 1;
}

.p-style > p:nth-child(1) {
  font-size: 70px;
  font-weight: 700;
}

@media (max-width: 1200px) {
  .statistics {
    column-gap: 100px;
  }
}

@media (max-width: 800px) {
  .statistics {
    grid-template-columns: auto;
    grid-template-rows: auto auto auto auto;
  }
}
</style>

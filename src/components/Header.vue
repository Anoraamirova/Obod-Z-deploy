<template>
 
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
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
    };
  },
  methods: {
    menuItems() {
      return this.menu;
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
}
.toolb {
  padding: 0 5%;
  text-align: center;
  background-image: linear-gradient(to right, #19d3dc, #18e7d3, #18e7d3, #19d2dd);
}
</style>

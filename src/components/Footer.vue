<template>
  <v-footer height="auto" class="toolb">
      <v-layout justify-center row wrap>
        <v-flex color="indigo" dark py-3 text-xs-center white--text xs12>
          &copy;2020 —
          <a
            href="http://it-solutions.uz"
            style="text-decoration:none; color: white"
            ><strong>IT-Solutions</strong></a
          >
        </v-flex>
      </v-layout>
    </v-footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    msg: String
  }
};
</script>

<style scoped>
* {
  margin: 0;
}
.toolb {
  padding: 0 5%;
  text-align: center;
  background-image: linear-gradient(
    to right,
    #19d3dc,
    #18e7d3,
    #18e7d3,
    #19d2dd
  );
}


</style>
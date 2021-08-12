<template>
  <div id="app">
    <Header @sendEmit="getEmit" />
    <Main :emitText="emitText" :emitType="emitType" />
    <div>
      <!-- <p>Comedy: {{ comedyArr.length }}</p> -->
      <!-- <pre>{{ comedyArr }}</pre> -->
      <!-- <p>Drama: {{ dramaArr.length }}</p>
      <p>Thriller: {{ thrillerArr.length }}</p> -->
    </div>
  </div>
</template>

<script>
/* Componenti */
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
/* Axios */
/* import axios from "axios"; */
export default {
  name: "App",
  data() {
    return {
      emitText: "",
      emitType: "",
    };
  },
  components: {
    Header,
    Main,
  },
  methods: {
    getEmit(obj) {
      this.emitText = obj.text;
      this.emitType = obj.type;
      console.log("emit text: ", this.emitText);
      console.log("emit Type: ", this.emitType);
    },
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background-color: black;
  color: white;
  font-family: "Montserrat", sans-serif;
}

a {
  color: white;
  text-decoration: none;
}
</style>

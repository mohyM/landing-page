<template>
  <div class="Body">
    <p class="name"> 
    Nam Tr
    <span v-if="vietname" @mouseleave="toggleName">ầ</span>
    <span v-if="!vietname" @mouseover="toggleName">a</span>
    n </p>
    <NavBar />
  </div>
</template>

<script>
import NavBar from './NavBar'
import '@fortawesome/fontawesome-free/css/all.css'
import '@fortawesome/fontawesome-free/js/all.js'
export default {
  name: 'Body',
  components: {
    NavBar,
  },
  props: {
    msg: String
  },
  data: function() {
    return {
      vietname: false
    }
  },
  methods: {
    toggleName() {
      this.vietname = !this.vietname;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Arsenal&display=swap");

* {
  font-family: 'Arsenal';
  text-align: center;
}

.Body {
  position: absolute;
  z-index: 2;
  top: 50%;
  left: 0;
  right: 0;
  transform: translateY(-50%);
}

.name {
  font-size: 8vw;
  margin: 0;
  padding: 0;
  /* letter-spacing: 3px; */
}

span {
  margin: -1.8vw;
  padding: 0;
  display: inline;
}

</style>

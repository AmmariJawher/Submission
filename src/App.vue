<template>
  <div id="app">
     <UsrMsg @inputData="updateMessage" />
    <PosterBox/>
    <PostItem />
  </div>
</template>

<script>
import PosterBox from "./components/PosterBox.vue";
import PostItem from "./components/PostItem.vue";

export default {
  name: "app",
  components: {
    PosterBox,
    PostItem
  },
  data: function() {
    return {
      childData: ""
    };
  },
  methods: {
    updateMessage(variable) {
      this.childData= variable;
    }
  }
};
</script>

<style lang="scss">
@import "../node_modules/bulma/css/bulma.css";
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

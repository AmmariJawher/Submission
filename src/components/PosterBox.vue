<template>
  <div id="post" class="section">
    <article class="media">
      <figure class="media-left">
        <img class="image is-64x64 is-rounded" src="https://pbs.twimg.com/media/D-zZHDSXYAA5Rkl.jpg"/>
      </figure>
      <div class="media-content">
        <textarea class="textarea" placeholder="e.g. Hello world" @keyup.enter="submit" v-model="tempPost"></textarea>
      </div>
      <div class="media-right">
        <a class="button is-primary" v-on="tempPost">Post</a>
      </div>
    </article>
  </div>  
</template>

<script>
export default {
  data() {
    return {
      tempPost: "",
    }
  },
  methods: {
    submit() {
      this.$emit("inputData", this.tempPost);
      this.tempPost = "";
    }
  }
}
</script>

<style lang="scss">

</style>

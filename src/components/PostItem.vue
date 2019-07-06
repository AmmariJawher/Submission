<template>
  <div id="post" class="section">
    <article class="media" v-for="post in posts" :key="post.id">
      <figure class="media-left">
        <img class="image is-64x64" :src="post.postPic" />
      </figure>
      <div class="media-content">
        <div class="content">
          <p>
            <strong>
              <a href="#" class="has-text-info">{{ post.name }}</a>
              <span class="tag is-small">#{{ post.rank }}</span>
            </strong>
            <br />
            {{ post.paragraph }}
            <br />
            <small class="is-size-7">
              Submitted by:
              <img
                class="image is-24x24"
                src="../assets/img/profile-pic1.jpg"
              />
            </small>
          </p>
        </div>
      </div>
      <div class="media-right">
        <span class="icon is-small">
          <i class="fa fa-chevron-up"></i>
          <strong class="has-text-info">10</strong>
        </span>
      </div>
    </article>
  </div>
</template>

<script>
export default {
  name: "PostItem",
  data: function() {
    return {
      posts: [
        {
          name: "David Bowie",
          paragraph: "I am an agilator, I am mama papa coming for you",
          profilePic: "../assets/img/profile-pic1.jpg",
          postPic: "https://www.shareicon.net/data/128x128/2016/09/01/822715_user_512x512.png",
          rank: 5,
          votes: 10
        },
        {
          name: "James Dean",
          paragraph: "is this the real life or it's just fantasy",
          profilePic: "../assets/img/profile-pic2.jpg",
          postPic: "https://www.shareicon.net/data/128x128/2016/08/18/810223_user_512x512.png",
          rank: 4,
          votes: 10
        }
      ]
    };
  }
};
</script>

<style lang="sass"></style>

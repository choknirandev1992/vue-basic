<template>
  <nuxt-link :to="postLink" class="post-preview">
      <article>
          <div
          class="post-thumnail"
          :style="{backgroundImage:'url('+thumbnail+')'}"></div>
              <div class="post-content">
                  <h1>{{ title }}</h1>
                  <p>{{ PreviewText }}</p>
              </div>
      </article>
  </nuxt-link>
</template>

<script>
export default {
  name : 'PostPreview',
  props: {
    id: {
      type: String,
      required: true
    },
    isAdmin:{
       type: Boolean,
       default: true
    },
    title: {
      type: String,
      required: true
    },
    PreviewText: {
      type: String,
      required: true
    },
    thumbnail: {
      type: String,
      required: true
    }
  },
  computed:{
     postLink(){
        return this.isAdmin ? '/admin/' + this.id : '/posts/' + this.id
     }
  }
}
</script>

<style>

.intro {
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}

.post-thumnail {
    height: 200px;
    background-size: cover;
    background-position: center center;
}

.intro h1 {
    position: static;
    top: 10%;
    width: 100%;
    color: black;
    background-color: rgb(211, 211, 211);
    padding: 10px;
    border-radius: 10px;
    box-shadow: 3px 3px 3px black;
    box-sizing: border-box;
    border: 1px solid black;
    text-align: center;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

.post-preview {
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 90%;
}

a {
  text-decoration: none;
  color: black;
}

@media (min-width: 850px) {
  .post-preview {
    width: 400px;
    display: block;
    margin: 0 auto 10px;
  }
}

.post-thumbnail {
  width: 100%;
  height: 200px;
  background-position: center;
  background-size: cover;
}

.post-content {
  padding: 10px;
  text-align: center;
}

a:hover .post-content,
a:active .post-content {
  background-color: #ccc;
}
</style>

<template>

     <section class="post-list">

      <PostPreview
         id="1"
         :is-admin="isAdmin"
         thumbnail="https://wallpaperaccess.com/full/158826.jpg"
         title="Hello"
         PreviewText="chokniran"
       />

       <PostPreview
         id="1"
         :is-admin="isAdmin"
         thumbnail="https://wallpaperaccess.com/full/158826.jpg"
         title="Hello"
         PreviewText="chokniran"
       />

       <PostPreview
         id="1"
         :is-admin="isAdmin"
         thumbnail="https://wallpaperaccess.com/full/158826.jpg"
         title="Hello"
         PreviewText="chokniran"
       />

     </section>

</template>

<script>

import  PostPreview  from '@/components/Posts/PostPreview'

export default {
  components: {
      PostPreview
  },
  props:{
    isAdmin:{
       type: Boolean,
       default: false
    }
  }
}

</script>

<style scoped>
 .post-page{
        display : flex;
        justify-content : center;
        align-items: center;
    }

  .post-list{
    padding: 20px;
  }
</style>

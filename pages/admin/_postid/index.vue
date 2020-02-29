<template>
  <div class="admin-post-page">
     <section class="update-form">
        <AdminPostForm :post="loadedPost"/>
     </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm'

export default {
  components: {
    AdminPostForm
  },
  data(){
     return {
       loadedPost: {
         author: 'Chokniran',
         title: 'wordpress',
         content: 'Web Content Management',
         thumbnailLink: 'https://wallpaperaccess.com/full/158826.jpg'

       }
     }
  }
}
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>

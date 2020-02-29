<template>
  <div class="post-page">
         <PostList/>
  </div >
</template>

<script>

import  PostList  from '@/components/Posts/PostList'

export default {
  components: {
      PostList
  }
}

</script>
<style scope>
    .post-page{
        display : flex;
        justify-content : center;
        align-items: center;
    }
</style>

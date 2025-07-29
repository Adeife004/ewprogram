<template>
 <div class="blog_container">
  <div class="blog_container_1">
    <div class="blog_img">
      <img src="../assets/platform.jpg" alt="img">
    </div>
    <div class="blog_post">
      <div><i class="bi bi-clock-fill"></i>
      <p>2 years ago</p>
    </div>
    <div><i class="bi bi-chat-fill"></i>
      <p>0 comment</p>
    </div>
    </div>
    <div class="blog_header">
      <h1>Platform Upgrade for Better User Experience</h1>
    </div>
    <div class="blog_link">
      <p>Read more</p>
      <i class="bi bi-arrow-right"></i>
    </div>
  </div>
  <div class="blog_container_2">
    <div class="blog_img">
      <img src="../assets/new_investment.jpg" alt="img">
    </div>
    <div class="blog_post">
      <div><i class="bi bi-clock-fill"></i>
      <p>2 years ago</p>
    </div>
    <div><i class="bi bi-chat-fill"></i>
      <p>0 comment</p>
    </div>
    </div>
    <div class="blog_header">
      <h1>New Investment Plans Launched</h1>
    </div>
    <div class="blog_link">
      <p>Read more</p>
      <i class="bi bi-arrow-right"></i>
    </div>
  </div>
 </div>
  <BlogList />

<script>
import BlogList from '../components/BlogList.vue'
export default {
  name: 'BlogView',
  components: { BlogList },
}
</script>

<style scoped>
.blog_container{
  padding-top:4cm !important;
  background-color: #151515;
  display: flex;
  row-gap: 5%;
  column-gap: 5%;
  /* justify-content: start; */
  padding: 20px 40px;
}

.blog_container img{
  height: 40vh !important;
  width: 100%;
  border-radius: 10px;
}

.blog_container_1{
  width: 30%;
  height: 70vh;
  background-color: #202020;
  padding: 10px;
  border-radius: 10px;
}

.blog_container_2{
  width: 30%;
  height: 70vh;
  background-color: #202020;
  padding: 10px;
  border-radius: 10px;
}

.blog_post div{
  display: flex;
  align-items: center;
  gap: 10px;
}

.blog_post{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 5px;
}

.blog_header{
  padding: 10px 5px;
  border-bottom: 2px solid #b0afaf4f;
  color: white;
}

.blog_header h1{
  width: 90%;
  font-weight: 800;
}

.blog_link{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 5px;
}

.blog_link p,
.blog_link i{
  color: white;
  font-weight: 800;
}

.blog_post i{
  color: rgb(255, 13, 0);
  font-size: 20px;
}

.blog_post p{
  color: white;
}

@media screen and (max-width: 1200px){
  *{
    padding: 0;
    margin: 0;
  }
  
  .blog_container{
  padding-top:4cm !important;
  background-color: grey;
  display: flex;
  flex-direction:column;
  row-gap: 1cm;
 
}

.blog_container_1,
.blog_container_2{
  width: 100%;
}

.blog_header h1{
  font-size: clamp(12px, 3vh, 17px);
}

}


</style>

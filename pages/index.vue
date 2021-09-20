<template>
<div>
  <Header />
  <p>Hello.</p>
  <!-- WRONG: <a href="/users">User Welcome Screen.</a> WILL LOAD A FRESH PAGE FROM SERVER-->
  <!-- RIGHT --> 
  <nuxt-link v-show='false' to="/users/">Users No-Reload</nuxt-link> <!--creates anchor tag, catches clicks before they are sent to server-->
  <nuxt-link v-show='false' to="/products/">Products Index</nuxt-link> 
  <section class='intro'>
    <h1>Get the latest news!</h1>
  </section>
  <section class='featured-posts'>
    <PostPreview 
      id="1" 
      thumbnail=""
      title="Hello 1"
      previewText="My first post" />
  </section>
</div>
</template>

<script>
//use '@' instead of '../'
import Header from '@/components/Header.vue'
import PostPreview from '@/components/Posts/PostPreview.vue'
export default {
  components: {
    Header,
    PostPreview
  }
}
</script>

<style>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
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
</style>
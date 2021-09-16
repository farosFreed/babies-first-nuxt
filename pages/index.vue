<template>
<div>
  <p>Hello.</p>
  <a href="/users">User Welcome Screen.</a> <!--WILL LOAD A FRESH PAGE FROM SERVER-->
  <nuxt-link to="/users">Users No-Reload</nuxt-link> <!--creates anchor tag, catches clicks before they are sent to server-->

  <nuxt-link to="/products">Products Index</nuxt-link> <!--creates anchor tag, catches clicks before they are sent to server-->
</div>
</template>

<script>
export default {}
</script>

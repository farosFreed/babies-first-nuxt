
<template>
<div>
  <p>Hello {{ pid }}</p>
  
</div>
</template>

<script>
export default {
    data() {
        return {
            pid: this.$route.params.id
        }
    }
}
</script>

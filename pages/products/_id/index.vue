
<template>
<div>
  <p>Hello {{ pid }}</p>
  
</div>
</template>

<script>
export default {
    validate (data) {
        return data.params.id == 1 //only 1 is valid id
    },
    data() {
        return {
            pid: this.$route.params.id
        }
    }
}
</script>

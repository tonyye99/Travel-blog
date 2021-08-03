<template>
  <h1>This is blog slug page</h1>
</template>
<script>
export default {
  mounted() {
    console.log(this.$route.params)
  },
}
</script>

<template>
  <div class="heading">
    <h1>{{ appName }}</h1>
  </div>
</template>

<script>
export default {
  name: "MyHeader",
  props: {
    appName: String,
  },
};
</script>

<style scoped>
.heading {
  text-align: center;
  padding: 1em 0;
}
</style>

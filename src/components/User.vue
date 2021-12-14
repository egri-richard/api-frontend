<template lang="html">
  <div class="user">
    <h1>{{ info.name }}</h1>
    <h3>{{ info.gender }}</h3>
    <h3>{{ info.age }}</h3>
  </div>
</template>

<script>
export default {
  name: "User",
  props: {info: Object}
}
</script>

<style lang="css" scoped>
.user {
  display: inline-block;
  width: 100px;
  height: 160px;
  margin: 10px 10px 10px 10px;
  padding-left: 10px;
  padding-right: 10px;
  box-shadow: 10px 10px 10px grey;
  background-color: rgb(245, 245, 245);
  transition: 0.2s;
}

.user:hover {
  transform: scale(1.1);
}

</style>

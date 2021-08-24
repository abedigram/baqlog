<template>
  <ul>
    <li v-for="leave in data" :key="leave.title">
      <leave :data="leave"></leave>
    </li>
  </ul>
</template>

<script>
export default {
  name: "tree",
  props: ["data"],
};
</script>

<style>
</style>
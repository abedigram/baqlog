<template>
  <div>
    <p>{{ data.title }}</p>
    <tree :data="data.children" v-if="data.children.length"></tree>
  </div>
</template>

<script>
import Tree from "~/components/tree";
export default {
  components: {
    Tree,
  },
  name: "leave",
  props: ["data"],
};
</script>

<style>
</style>

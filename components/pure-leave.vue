<template>
  <div>
    <p>{{ data.title }}</p>
    <PureTree :data="data.children" v-if="data.children.length" />
  </div>
</template>

<script>
import PureTree from "~/components/pure-tree.vue";
export default {
  components: {
    PureTree,
  },
  name: "PureLeave",
  props: ["data"],
};
</script>

<style>
</style>
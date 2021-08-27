
<template>
  <ul>
    <li v-for="leave in data" :key="leave.title">
      <!-- {{ leave }} -->
      <PureLeave :data="leave" />
    </li>
  </ul>
</template>

<script>
import PureLeave from "~/components/pure-leave.vue";
export default {
  components: {
    PureLeave,
  },
  name: "PureTree",
  props: ["data"],
};
</script>

<style scoped>
ul {
  display: block;
  background-color: lightgray;
  border: 1px solid gray;
  box-sizing: border-box;
  padding: 5px !important;
  list-style: none;
}
</style>
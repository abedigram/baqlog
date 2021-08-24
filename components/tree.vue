<template>
  <!-- <ul>
    <li v-for="leave in data" :key="leave.title">
    </li>
  </ul> -->

  <v-expansion-panels v-model="opens" multiple>
    <v-expansion-panel v-for="(leave, i) in data" :key="i" multiple>
      <v-expansion-panel-header>
        <v-text-field
          :value="leave.title"
          @click.stop
          outlined
          dense
          class="textf"
        ></v-text-field>
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <tree :data="leave.children" v-if="leave.children.length"></tree>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>

<script>
export default {
  name: "tree",
  props: ["data"],
  data: () => {
    return {
      opens: [],
    };
  },
};
</script>

<style>
.textf fieldset {
  border: none !important;
}
</style>

<style scoped>
</style>

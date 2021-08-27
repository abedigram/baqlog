<template>
  <v-row justify="center">
    <v-col xl="2" lg="3" md="5" sm="10" cols="12">
      <PureTree :data="tree" />
    </v-col>
  </v-row>
</template>

<script>
import PureTree from "~/components/pure-tree.vue";
export default {
  components: {
    PureTree,
  },
  data: () => {
    return {
      tree: [
        {
          id: "12234",
          title: "silvester",
          children: [
            {
              id: "122484",
              title: "jack-J",
              children: [
                {
                  id: "122484",
                  title: "jackC1",
                  children: [],
                },
                {
                  id: "124824",
                  title: "jackC2",
                  children: [
                    {
                      id: "12484",
                      title: "jackCC2",
                      children: [],
                    },
                  ],
                },
              ],
            },
            {
              id: "124844",
              title: "jack-JJ",
              children: [],
            },
          ],
        },
        {
          id: "12434",
          title: "john",
          children: [
            {
              id: "1248254",
              title: "jack-jo",
              children: [
                {
                  id: "123484",
                  title: "jack-movie",
                  children: [],
                },
              ],
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
</style>
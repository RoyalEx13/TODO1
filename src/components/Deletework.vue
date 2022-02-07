<template>
  <v-container>
    <v-row>
      <v-list class="mx-5">
        <v-subheader>รายการที่เพิ่ม</v-subheader>
        <v-list-item-group v-model="selectedItem" color="primary">
          <v-list-item v-for="(item, i) in tt" :key="i">
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.awk"></v-list-item-title>
            </v-list-item-content>
            <v-btn icon color="red" class="mx-10" @click="deletestu(i)">
              <v-icon right>mdi-cancel</v-icon>
            </v-btn>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: ["tt"],

  data() {
    return {};
  },
  methods: {
    deletestu(index) {
      this.tt.splice(index, 1);
    },
  },
};
</script>

<style></style>

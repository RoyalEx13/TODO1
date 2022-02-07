<template>
  <v-container>
    <h1>การบ้าน/ งานที่ได้รับหมอบหมาย</h1>
    เพิ่มงาน
      <v-row>
        <v-col class="text-md mx-3">
          <v-select
            :items="items"
            label="วิชา"
            id="clas"
            v-model="clas"
            
          ></v-select>
        </v-col>
        <v-col class="text-md mx-3">
          <v-text-field
            label="ชื่องาน"
            :rules="rules"
            hide-details="auto"
            id="work"
            v-model="work"
            required
          ></v-text-field>
        </v-col>
        <v-col>
          <v-btn color="primary" class="mr-4" @click="addstu(subject,work)">Add</v-btn>
        </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      subject: "",
      work: "",
      items: ["วิชา Web", "วิชา SA", "วิชา ML", "อื่นๆ"],
      selectedItem: 1,
      additems: "",
      rules: [
        (value) => !!value || "Required.",
        (value) => (value && value.length >= 3) || "Min 3 characters",
      ],
      list: [
        { awk: "วิชา Web Assignment500", icon: "mdi-clock" },
        { awk: "วิชา ML Assignment1", icon: "mdi-clock" },
        { awk: "วิชาML ออกแบบ", icon: "mdi-clock" },
        { awk: "วิชา Web Assignment501", icon: "mdi-clock" },
      ],
    };
  },
  methods: {
      addstu: function (subject, work) {
      this.list.push({ awk: subject + " " + work, icon: "mdi-clock" });
      this.$emit("rtb", this.additems);
    },
    },
};
</script>

<style></style>

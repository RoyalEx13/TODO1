<template>
  <div>
    <Addwork @rtb="Add"></Addwork>
    <Deletework :tt="list"></Deletework>
  </div>
</template>

<script>
import Addwork from "../components/Addwork.vue";
import Deletework from "../components/Deletework.vue";
export default {
  data() {
    return {
      list: [
        { awk: "วิชา Web Assignment500", icon: "mdi-clock" },
        { awk: "วิชา ML Assignment1", icon: "mdi-clock" },
        { awk: "วิชาML ออกแบบ", icon: "mdi-clock" },
        { awk: "วิชา Web Assignment501", icon: "mdi-clock" },
      ],
    };
  },
  components: { Addwork, Deletework },
  methods: {
    Add(subject,work) {
      this.list.push({ awk: subject + " " + work, icon: "mdi-clock" });
    },
  },
};
</script>

<style></style>

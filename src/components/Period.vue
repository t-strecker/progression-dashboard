<template>
  <div class="period-container">
    <div class="title">{{ title }}</div>
    <div class="begin-date">{{ formatDate(beginDate) }}</div>
    <div class="end-date">{{ formatDate(endDate) }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { formatDate } from "@/utils/date-utils";

export default defineComponent({
  name: "Period",
  props: {
    title: String,
    beginDate: String,
    endDate: String,
  },
  methods: {
    formatDate,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.period-container {
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
}
.title {
  font-size: 16px;
  font-weight: bold;
}
.begin-date,
.end-date {
  position: absolute;
  font-weight: bold;
  font-size: 12px;
  bottom: -20px;
}
.begin-date {
  left: 0;
}
.end-date {
  right: 0;
}
</style>

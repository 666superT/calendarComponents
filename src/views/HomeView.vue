<template>
  <div class="home">
    <MyDate
      :markDays="markDays"
      :disabledAfter="disabledAfter"
      :selectDate="selectDate"
      :weekstart="weekstart"
      @changeMonth="changeMonth"
      @setDate="setDate"
    ></MyDate>
  </div>
</template>

<script>
import MyDate from "@/components/MyDate";
export default {
  components: {
    MyDate,
  },
  data() {
    return {
      // 标记日期
      markDays: [
        { type: "yes", date: "2022-09-21" },
        { type: "no", date: "2022-09-10" },
      ],
      // 未来日期是否不可点击
      disabledAfter: true,
      // 默认选中日期
      selectDate: "2022-09-15",
      // 星期几为第一天
      weekstart: 1,
    };
  },
  methods: {
    // 改变月份时触发
    changeMonth(date) {
      console.log(date);
    },
    // 点击获取日期
    setDate(date) {
      console.log(date);
    },
  },
};
</script>

<style lang="scss" scoped>
// .home {
//   width: 500px;
//   margin: 50px auto;
// }
</style>

<template>
  <div class="page-index">
    <el-row>
      <!-- 全部分类 -->
      <el-col :span="5">
        <m-menu />
      </el-col>
      <el-col :span="19">
        <m-life />
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <!-- 有格调 -->
        <container :nav="iStyle" />
      </el-col>
      <el-col :span="24">
        <!-- 很优惠 -->
        <container :nav="recomment" />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import MMenu from "@/components/index/menu";
import MLife from "@/components/index/life";
import Container from "@/components/index/container.vue";

export default {
  data() {
    return {
      iStyle: {
        class: "istyle",
        title: "有格调",
        list: [
          {
            text: "全部",
            tab: "all"
          },
          {
            text: "约会聚餐",
            tab: "food"
          },
          {
            text: "丽人SPA",
            tab: "spa"
          },
          {
            text: "电影演出",
            tab: "movie"
          },
          {
            text: "品质出游",
            tab: "travel"
          }
        ]
      },
      recomment: {
        class: "youhui",
        title: "很优惠",
        list: [
          {
            text: "全部",
            tab: "all"
          },
          {
            text: "美食",
            tab: "food"
          },
          {
            text: "休闲",
            tab: "xiuxian"
          }
        ]
      }
    };
  },
  components: {
    MMenu,
    MLife,
    Container
  }
};
</script>

<style lang="scss">
@import "@/assets/css/index/index.scss";
</style>
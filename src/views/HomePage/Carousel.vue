<template>
    <div class="block">
      <el-carousel height="600px" arrow="always">
        <el-carousel-item v-for="(item,index) in items" :key="index">
          <img :src="item" style="width: 100%; height: 100%;"/>
        </el-carousel-item>
      </el-carousel>
    </div>
</template>

<script>
    export default {
      data() {
        return {
          items: [require('../../assets/bg-images/bg01.png'),require('../../assets/bg-images/bg02.png'),require('../../assets/bg-images/bg03.png')]
        }
      }
    }
</script>

<style>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }
</style>

<template>
  <div class="app" id="app">
       <div class="banner">
      <img class="hidden-xs-only hidden-sm-only hidden-lg-only hidden-xl-only" :src="bannerMD" alt="banner 图">
    </div>
    <!-- 第一行 -->
    <el-row>
      <el-col :xs="24" :sm="24" :md="10" :lg="10" :xl="10" class="part">
        <router-view name="PartOne"/>
      </el-col>
      <el-col :xs="24" :sm="24" :md="14" :lg="14" :xl="14" class="part">
        <router-view name="PartTwo"/>
      </el-col>
      
    </el-row>
    <!-- 第二行 -->
    <el-row>
      <el-col :xs="24" :sm="24" :md="12" :lg="12" :xl="12" class="part">
        <router-view name="PartThree"/>
      </el-col>
      <el-col :xs="24" :sm="24" :md="12" :lg="12" :xl="12" class="part">
        <router-view name="PartFour"/>
      </el-col>
    </el-row>
      <!-- 第三行 -->
    <el-row>
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8" class="part">
        <router-view name="PartFive"/>
      </el-col>
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8" class="part">
        <router-view name="PartSix"/>
      </el-col>
      <el-col :xs="24" :sm="24" :md="8" :lg="8" :xl="8" class="part">
        <router-view name="PartSeven"/>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      bannerMD: require("./assets/img/banner_1000.png"),  
    }
  }
}
</script>

<style>
body {
  background: #011128;
  color: #fff;
}
.app {
  width: 100%;
}
.part {
  padding: 20px;
}
.banner img {
  width: 100%;
  height: 80px;
}
p {
  text-align: center;
}
</style>

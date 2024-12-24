<!-- ComparisonBar.vue -->

<template>
  <div class="comparison-bar">
    <!-- 对于每一个比较案例，创建一行 -->
    <el-row :gutter="20" v-for="(comparison, index) in comparisons" :key="index" class="comparison-row">
      <!-- 参考图像 -->
      <el-col :span="4">
        <div class="reference-image">
          <el-image :src="comparison.referenceImage" fit="contain" />
        </div>
      </el-col>
      <!-- 姿势GIF -->
      <el-col :span="4">
        <div class="pose-gif">
          <el-image :src="comparison.poseGif" fit="contain" />
        </div>
      </el-col>
      <!-- ControlNext GIF -->
      <el-col :span="8">
        <div class="comparative-video">
          <el-image :src="comparison.comparativeVideo1" fit="contain" />
        </div>
      </el-col>
      <!-- EnergyVid GIF -->
      <el-col :span="8">
        <div class="comparative-video">
          <el-image :src="comparison.comparativeVideo2" fit="contain" />
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'ComparisonBar',
  data() {
    return {
      comparisons: [
        {
          referenceImage: "./comparison/case1/reference.jpg",
          poseGif: "./comparison/case1/pose.gif",
          comparativeVideo1: "./comparison/case1/controlnext.gif",
          comparativeVideo2: "./comparison/case1/energyvid.gif",
        },
        {
          referenceImage: "./comparison/case2/reference.png",
          poseGif: "./comparison/case2/pose.gif",
          comparativeVideo1: "./comparison/case2/controlnext.gif",
          comparativeVideo2: "./comparison/case2/energyvid.gif",
        },
        {
          referenceImage: "./comparison/case3/reference.jpg",
          poseGif: "./comparison/case3/pose.gif",
          comparativeVideo1: "./comparison/case3/controlnext.gif",
          comparativeVideo2: "./comparison/case3/energyvid.gif",
        },
      ]
    }
  }
}
</script>

<style scoped>
.comparison-bar {
  padding: 20px;
}

.comparison-row {
  margin-bottom: 40px;
}

.reference-image,
.pose-gif,
.comparative-video {
  text-align: center;
}

.reference-image .el-image,
.pose-gif .el-image,
.comparative-video .el-image {
  max-width: 100%;
  height: auto;
}
</style>

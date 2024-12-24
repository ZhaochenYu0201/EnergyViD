<!-- ComparisonBar.vue -->

<template>
  <div class="comparison-bar">
    <el-row :gutter="20">
      <el-col :span="8" v-for="(comparison, index) in comparisons" :key="index">
        <div class="comparison-column">
          <!-- 参考图像 -->
          <div class="reference-image">
            <el-image :src="comparison.referenceImage" fit="contain" />
          </div>
          <!-- 姿势GIF -->
          <div class="pose-gif">
            <el-image :src="comparison.poseGif" fit="contain" />
          </div>
          <!-- 对比视频GIF -->
          <div class="comparative-videos">
            <el-image :src="comparison.comparativeVideo1" fit="contain" />
            <el-image :src="comparison.comparativeVideo2" fit="contain" />
          </div>
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
          comparativeVideo1: "./comparison/case1/controlnext.gif",
          comparativeVideo2: "./comparison/case1/energyvid.gif",
        },
        {
          referenceImage: "./comparison/case3/reference.jpg",
          poseGif: "./comparison/case3/pose.gif",
          comparativeVideo1: "./comparison/case1/controlnext.gif",
          comparativeVideo2: "./comparison/case1/energyvid.gif",
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
.comparison-column {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.reference-image,
.pose-gif,
.comparative-videos {
  margin-bottom: 15px;
}
.comparative-videos {
  display: flex;
  justify-content: center;
}
.comparative-videos .el-image {
  margin: 0 5px;
}
</style>

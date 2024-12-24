<template>
  <section class="video-slider-section">
    <h2>Compare with SOTA method ControlNeXt on Pose and FaceID</h2>
    <div class="video-slider">
      <!-- 左侧切换按钮 -->
      <button @click="prevVideo" class="slider-button left-button" aria-label="Previous Video">＜</button>

      <!-- 视频播放区域 -->
      <video :src="currentVideo" controls autoplay></video>

      <!-- 右侧切换按钮 -->
      <button @click="nextVideo" class="slider-button right-button" aria-label="Next Video">＞</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'VideoSlider',
  data() {
    return {
      // 视频数组，包含三个视频的路径
      videos: [
        require('@/video_slider/case1.mp4'),
        require('@/video_slider/case2.mp4'),
        require('@/video_slider/case3.mp4'),
      ],
      // 当前视频的索引
      currentIndex: 0,
    };
  },
  computed: {
    // 计算属性，获取当前播放的视频
    currentVideo() {
      return this.videos[this.currentIndex];
    },
  },
  methods: {
    // 切换到上一个视频
    prevVideo() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
      } else {
        // 如果已经是第一个视频，跳转到最后一个
        this.currentIndex = this.videos.length - 1;
      }
    },
    // 切换到下一个视频
    nextVideo() {
      if (this.currentIndex < this.videos.length - 1) {
        this.currentIndex++;
      } else {
        // 如果已经是最后一个视频，跳转到第一个
        this.currentIndex = 0;
      }
    },
  },
};
</script>

<style scoped>
.video-slider-section {
  margin-top: 40px;
  text-align: center;
}

.video-slider {
  position: relative;
  display: inline-block;
}

.slider-button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: transparent;
  border: none;
  font-size: 2em;
  cursor: pointer;
  z-index: 1;
  color: #333;
}

.left-button {
  left: -50px;
}

.right-button {
  right: -50px;
}

.video-slider video {
  max-width: 100%;
}

.slider-button:hover {
  color: #000;
}
</style>

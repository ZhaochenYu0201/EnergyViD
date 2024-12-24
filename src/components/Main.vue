<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Carousel from './sections/Carousel.vue'
import ImageSlider from './sections/ImageSlider.vue'
import Echart from './sections/Echart.vue'
import Table from './sections/Table.vue'
import Collapse from './sections/Collapse.vue'
import SeletionForComparison from './sections/SeletionForComparison.vue'
import VideoSlider from './sections/video_slider.vue'  // 引入新组件

export default {
  components: {
    Title,
    Abstract,
    Carousel,
    ImageSlider,
    Echart,
    Collapse,
    Table,
    SeletionForComparison,
    VideoSlider,  // 注册新组件
  }
}
</script>

<template>
  <Title/>
  <Carousel/>
  <Abstract/>
  <Echart/>
  <Table/>
  <Collapse/>
  <VideoSlider/>  <!-- 使用新组件 -->
  <SeletionForComparison/>
  <ImageSlider/>
</template>

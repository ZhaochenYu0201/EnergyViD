<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Carousel from './sections/Carousel.vue'
import ImageSlider from './sections/ImageSlider.vue'
import Echart from './sections/Echart.vue'
import Table from './sections/Table.vue'
import Collapse from './sections/Collapse.vue'
import SeletionForComparison from './sections/SeletionForComparison.vue'
import ComparisonBar from './sections/ComparisonBar.vue'  // 引入新组件

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
    ComparisonBar,  // 注册新组件
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
  <ComparisonBar/>  <!-- 添加新组件到模板 -->
  <SeletionForComparison/>
  <ImageSlider/>
</template>

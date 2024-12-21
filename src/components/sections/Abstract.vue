<script>

export default {
  data() {
    return {
      abstract: "Diffusion-based generative models have exhibited considerable success in conditional video synthesis and editing. Nevertheless, prevailing video diffusion models primarily rely on conditioning with specific input modalities, predominantly text, restricting their adaptability to alternative modalities without necessitating retraining of modality-specific components. In this work, we present EnergyViD, a universal spatio-temporal Energy-guided Video Diffusion model designed for zero-shot video synthesis and editing across diverse conditions. Specifically, we leverage off-the-shelf pre-trained networks to construct generic energy functions, guiding the generation process under specific conditions without the need for retraining. To precisely capture temporal dynamics related to motion conditions (e.g., pose sequences), we introduce a novel kernel Maximum Mean Discrepancy (MMD)-based energy function, which minimizes the global distribution discrepancy between the conditioning input and the generated video. Our extensive qualitative and quantitative experiments demonstrate that our algorithm consistently produces high-quality results across a wide range of motion and non-motion conditions, including text, face ID, style, poses, depths, sketches, canny edges, and segmentation maps, in the context of zero-shot video synthesis and editing. We will release source code upon acceptance of the paper."
    }
  }
}
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Abstract</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <p>{{ abstract }}</p>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>

/* 摘要文字居中 */
p {
  text-align: justify;
} 

</style>
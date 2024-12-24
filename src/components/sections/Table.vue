<script lang="ts" setup>

// 表格数据
const tableData = [
{
    model: 'Text2Video-Zero',
    Memory Usage: '6.2 GB',
    Inference Time: '30s',
},
{
    model: 'ControlVideo',
    Memory Usage: '6.8 GB',
    IInference Time: '3 min',
},
{
    model: 'ControlNeXt + SVD',
    Memory Usage: '30 GB',
    Inference Time: '20 min',
},
{
    model: 'Ours + Text2Video-Zero',
    Memory Usage: '8.7 GB',
    Inference Time: '2 min',
},
{
    model: 'Ours + SVD',
    Memory Usage: '12 GB',
    Inference Time: '8 min',
},
]
</script>

<template>
    <div>
        <el-divider />

        <el-row justify="center">
            <h1 class="section-title">Analysis of Memory Usage and Inference Time</h1>
        </el-row>
        
        <!-- 数据表格 -->
        <el-row justify="center">
            <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">

                <!-- 卡片 -->
                <el-card class="card">

                    <!-- 默认tab -->
                    <el-tabs class="demo-tabs" model-value="Method A">

                    <!-- 第一个tab -->
                    <el-tab-pane label="Method A" name="Method A">

                        <!-- 表格数据 -->
                        <el-table 
                            :data="tableData"
                            :default-sort="{ prop: 'value_b', order: 'descending' }"
                            scrollbar-always-on
                        >
                            <el-table-column prop="model" label="Model" width="100" sortable/>
                            <el-table-column prop="params" label="#Params" min-width="120" sortable/>
                            <el-table-column prop="value_a" label="Value A" min-width="120" sortable/>
                            <el-table-column prop="value_b" label="Value B" min-width="120" sortable/>
                        </el-table>
                    </el-tab-pane>

                    </el-tabs>

                </el-card>
            </el-col>
        </el-row>

    </div>
</template>

<style scoped>
.card {
    margin-top: 20px;
}
</style>
  
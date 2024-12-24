<script lang="ts" setup>

// 表格数据
const tableData = [
{
    Method: 'Text2Video-Zero',
    Memory: '6.2 GB',
    Time: '30s',
},
{
    Method: 'ControlVideo',
    Memory '6.8 GB',
    Time: '3 min',
},
{
    Method: 'ControlNeXt + SVD',
    Memory: '30 GB',
    Time: '20 min',
},
{
    Method: 'Ours + Text2Video-Zero',
    Memory: '8.7 GB',
    Time: '2 min',
},
{
    Method: 'Ours + SVD',
    Memory: '12 GB',
    Time: '8 min',
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
  
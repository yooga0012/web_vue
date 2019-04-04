<template>
    <section class="main">

        <video width="500px" height="500px" controls="true" src="http://192.168.3.20/group1/M00/00/06/wKgDFFylsxuALlPAAO4qwMnVkSs062.mp4"></video>
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item><i class="el-icon-rank"></i> 拖拽组件</el-breadcrumb-item>
                <el-breadcrumb-item>拖拽弹框</el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <div class="container">
            <p>通过指令 v-dialogDrag 使 Dialog 对话框具有可拖拽的功能。</p>
            <br>
            <el-button type="primary" @click="visible = true;">点我弹框</el-button>
        </div>
        <el-dialog v-dialogDrag title="拖拽弹框" center :visible.sync="visible" width="30%">
            我是一个可以拖拽的对话框！
            <span slot="footer" class="dialog-footer">
                <el-button @click="visible = false">取 消</el-button>
                <el-button type="primary" @click="visible = false">确 定</el-button>
            </span>
        </el-dialog>
    </section>
</template>

<script>
export default {
    data(){
        return {
            visible: false
        }
    }
}
</script>

<style>

</style>

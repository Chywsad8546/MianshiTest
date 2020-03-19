<template>
    <div class="top_bar" style="height: 70px;background-color: #EAC50B">
    <el-menu
            :default-active="activeIndex2"
            class="el-menu-demo"
            mode="horizontal"
            @select="handleSelect"
            background-color="#EAC50B"
            text-color="#FFFFFF"
            active-text-color="#FFFFFF"
            style="padding-left: 40px;padding-top: 5px">
        <el-menu-item index="1">订单消息</el-menu-item>
        <el-submenu index="2">
            <template slot="title">操作日志</template>
            <el-menu-item index="2-1">选项1</el-menu-item>
            <el-menu-item index="2-2">选项2</el-menu-item>
            <el-menu-item index="2-3">选项3</el-menu-item>
            <el-submenu index="2-4">
                <template slot="title">选项4</template>
                <el-menu-item index="2-4-1">选项1</el-menu-item>
                <el-menu-item index="2-4-2">选项2</el-menu-item>
                <el-menu-item index="2-4-3">选项3</el-menu-item>
            </el-submenu>
        </el-submenu>
        <el-menu-item index="3" disabled>系统信息</el-menu-item>
        <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">系统设置</a></el-menu-item>
    </el-menu>
        <div style=" padding-top: 3px;color: #FFFFFF ;font-size: 14px;position: relative;left: 40%;top: 10px">
            <i style="padding-right: 10px;font-size: 17px;"  class="el-icon-search"></i>
            <i style="padding-right: 10px;font-size: 17px;" class="el-icon-bell"></i>
            <el-avatar size="small" style="position: relative;
                              top: 8px;" src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar>
            <span style="padding-left: 10px;">用户名</span>
        </div>

    </div>
</template>


<script>

    export default {
        name: 'TopBar',
        data() {
            return {
                activeIndex2: '1'
            };
        },
        methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }

</script>
<style lang="less" scoped>
    .el-menu-item is-active{
        border-bottom-color:#EAC50B;
    }
</style>

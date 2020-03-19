<template>
    <el-col :span="4">
        <div style="
                    color: rgba(249, 248, 248, 1);
                    font-size: 25px;
                    text-align: left;
                    padding: 19px 0px 15px 45px;
                    font-family: SourceHanSansSC-regular;">
            公司LOGO
        </div>
        <el-menu
                default-active="2"
                class="el-menu-vertical-demo"
                @open="handleOpen"
                @close="handleClose"
                background-color="#383838"
                text-color="#fff"
                active-text-color="#ffd04b">
            <el-submenu index="1">
                <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>基础信息</span>
                </template>
                <el-menu-item-group>
                    <template slot="title">分组一</template>
                    <el-menu-item index="1-1">客户管理</el-menu-item>
                    <el-menu-item index="1-2">工序管理</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-3">
                    <template slot="title">银行账户管理</template>
                    <el-menu-item index="1-3-1">银行账户管理</el-menu-item>
                </el-submenu>
            </el-submenu>
            <el-submenu index="2">
                <template slot="title">
                    <i class="el-icon-location"></i>
                    <span>用户管理</span>
                </template>
                <el-menu-item index="2-1">内部用户</el-menu-item>
                <el-menu-item index="2-1">画师用户</el-menu-item>
            </el-submenu>
            <el-menu-item index="3" disabled>
                <i class="el-icon-document"></i>
                <span slot="title">画师管理</span>
            </el-menu-item>
            <el-menu-item index="4">
                <i class="el-icon-setting"></i>
                <span slot="title">订单管理</span>
            </el-menu-item>
            <el-menu-item index="5">
                <i class="el-icon-setting"></i>
                <span slot="title">分包管理</span>
            </el-menu-item>
            <el-menu-item index="6">
                <i class="el-icon-setting"></i>
                <span slot="title">收款管理</span>
            </el-menu-item>
            <el-menu-item index="7">
                <i class="el-icon-setting"></i>
                <span slot="title">付款管理</span>
            </el-menu-item>
        </el-menu>
    </el-col>
</template>


<script>

    export default {
        name: 'leftBar',
        data() {
            return {
                form: {},
                username: '',
            };
        },
        methods: {
            handleOpen(key, keyPath) {
                console.log(key, keyPath);
            },
            handleClose(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }

    </script>
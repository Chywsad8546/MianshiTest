<template>
    <div style="height: 100%;width: 100%">
        <leftBar style="height: 100%;background-color: #383838 " ></leftBar>
        <TopBar style="display: flex;"></TopBar>
        <el-breadcrumb style="display: flex;
    padding-left: 15px;
    padding-top: 10px;" separator="/">
            <el-breadcrumb-item :to="{ path: '/' }"><span style="color: #929292;font-size: 14px">基础信息</span></el-breadcrumb-item>
            <el-breadcrumb-item><a href="/"><span style="color: #929292;font-size: 14px">客户管理</span></a></el-breadcrumb-item>
        </el-breadcrumb>
        <div class="customer_table">
            <el-input
                    class="search-input"
                    style="width: 381px;    position: relative;
                           left: 35px;"
                    placeholder="输入客户名称/手机/邮箱"
                    prefix-icon="el-icon-search"
                    v-model="input2">
                <el-button slot="append" class="search-input-textbutton" type="text">搜索</el-button>
            </el-input>

            <el-button style="width: 117px;position: relative;
    left: 39%;" type="primary">新建客户</el-button>

            <el-select style="width: 165px;position: relative;
    left: 41%;" v-model="value" placeholder="更多">
                <el-option
                        v-for="item in options"
                        :key="item.value"
                        :label="item.label"
                        :value="item.value">
                </el-option>
            </el-select>
        </div>
        <div style="display: flex;margin-top: 40px">
            <el-table
                    :data="tableData"
                    stripe
                    style="width: 100%">
                <el-table-column
                        type="selection"
                        width="55">
                </el-table-column>
                <el-table-column
                        prop="date"
                        label="序号"
                        width="60"
                        >
                </el-table-column>
                <el-table-column
                        prop="name"
                        label="名称"
                       >
                    <template slot-scope="scope">
                       <span style="color: #1491FD "> {{ scope.row.name }}</span>
                    </template>
                </el-table-column>
                <el-table-column
                        prop="jibie"
                        label="级别">
                </el-table-column>
                <el-table-column
                        prop="laiyuan"
                        label="来源">
                </el-table-column>
                <el-table-column
                        prop="hangye"
                        label="行业">
                </el-table-column>
                <el-table-column
                        prop="phone"
                        label="电话">
                </el-table-column>
                <el-table-column
                        prop="email"
                        label="邮箱">
                </el-table-column>
                <el-table-column
                        prop="qq"
                        label="QQ">
                </el-table-column>
                <el-table-column
                        prop="wechat"
                        label="微信">
                </el-table-column>
                <el-table-column
                        prop="address"
                        label="联系地址">
                </el-table-column>
                <el-table-column
                        prop="fuzeren"
                        label="负责人">
                </el-table-column>
            </el-table>
        </div>

    </div>

</template>


<script>
    import leftBar from "./leftBar";
    import TopBar from "./TopBar";
    export default {
        name: 'CustomerList',
        components:{leftBar,TopBar},
        data() {
            return {
                options:[],
                tableData: [{
                    date: '1',
                    name: '北京宏',
                    jibie: '重点客户',
                    laiyuan: '广告',
                    hangye: '广告',
                    phone: '133333',
                    email: '133333@22',
                    QQ: '133334',
                    wechat: '133',
                    address: '北京市',
                    fuzeren:'管理员'
                },{
                    date: '1',
                    name: '北京宏',
                    jibie: '重点客户',
                    laiyuan: '广告',
                    hangye: '广告',
                    phone: '133333',
                    email: '133333@22',
                    QQ: '133334',
                    wechat: '133',
                    address: '北京市',
                    fuzeren:'管理员'
                },{
                    date: '1',
                    name: '北京宏',
                    jibie: '重点客户',
                    laiyuan: '广告',
                    hangye: '广告',
                    phone: '133333',
                    email: '133333@22',
                    QQ: '133334',
                    wechat: '133',
                    address: '北京市',
                    fuzeren:'管理员'
                }],
                input2:"",
                form:{

                },
                username: '',
            };
        },
        methods: {
            async logout() {

            },
        },
        created() {

        },
    };
</script>
<style lang="less" scoped>

    .search-input /deep/ .el-input__inner{
        border-radius: 53px;
        background-color: #f6f5f5;
    }
    .search-input /deep/ .el-input-group__append{
        position: relative;
        left: -77px;
        border-right: none;
        color: #0084FF;
    }
    .customer_table{
        display: flex;
        width: 83.33333%;
        margin-top: 40px;
    }
</style>

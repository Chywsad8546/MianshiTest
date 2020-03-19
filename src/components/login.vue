<template>
    <div class="main_body">
        <div style="z-index: 20 ;width: 100%;height: 100%">
            <div class="main_body_company_logo mask_on">
                公司LOGO
            </div>
            <div class="main_body_company_title mask_on">
                ARYA管理系统
            </div>

            <el-form class="main_body_company_form mask_on" style="position: absolute;width: 330px;
                            top: 370px;margin-left: calc(50% - 200px);" ref="form" :model="form" label-width="80px">
                <el-form-item label="账号:">
                    <el-input v-model="form.name"></el-input>
                </el-form-item>

                <el-form-item label="密码:">
                    <el-input v-model="form.name"></el-input>
                </el-form-item>
                <el-button style="width: 330px;
                           margin-top: 45px; color: rgba(16, 16, 16, 1);
                            font-size: 20px;
                            text-align: center;
                            font-family: Microsoft Yahei;">登录</el-button>
            </el-form>
            <!--<div class="main_body_company_form">
                <div class="center_set">
                    账号
                </div>
                <div class="center_set">
                    密码
                </div>
                <div class="center_set">
                    <el-button>登录</el-button>
                </div>
            </div>-->
        </div>
        <div class="main_body_mask">
        </div>
    </div>
</template>

<script>

    export default {
        name: '',
        data() {
            return {
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
    .main_body_company_form /deep/ .el-form-item__label{
        color: rgba(234, 197, 11, 1);
        font-size: 28px;
        text-align: left;
        font-family: SourceHanSansSC-regular;
    }

    .main_body_company_form /deep/ .el-form-item{
        border-bottom: 1px solid rgb(255, 255, 255);
    }




    .main_body_company_form /deep/ .el-input__inner{
        border: 0px;
        background:none;
        color: rgba(230, 223, 223, 1);
        font-size: 28px;
        text-align: left;
        font-family: SourceHanSansSC-regular;
    }

    .mask_on{
        z-index: 20;
    }
     .main_body{
         left: 0px;
         top: 0px;
         width: 100%;
         height: 100%;
         background-image: url("../assets/loginPage.png");
         background-repeat:no-repeat;
         background-position:center;
         background-size: cover;

          .main_body_mask{
              position: absolute;
              top: 0px;
              width: 100%;
              height: 100%;
              z-index: 10;
              background-color:#000000; opacity:0.5; -moz-opacity:0.5; filter:alpha(opacity=50);
          }

         .main_body_company_logo{
             left: 81px;
             top: 96px;
             width: 176px;
             height: 54px;
             color: rgba(255, 255, 255, 1);
             font-size: 36px;
             text-align: left;
             position: absolute;
             font-family: SourceHanSansSC-regular;
         }

             .main_body_company_title{
                 top: 173px;
                 text-align: center;
                 width: 100%;
                 position: absolute;
                 height: 50px;
                 color: rgba(234, 197, 11, 1);
                 font-size: 36px;
                 font-family: Roboto-regular;
             }
         .main_body_company_form{
             position: absolute;
             top: 375px;
             width: 100%;
         }
     }
    .center_set{
        text-align: center;
    }
</style>

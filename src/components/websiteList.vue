<!-- 学习网站列表 -->
<template>
    <div class="webSite">
        <div class="listView" v-for="(website,index) in websiteOptions.dataList" :key="index">
            <el-row class="HeadTitle">
                {{website.title}}
            </el-row>
            <el-row class="listItem">
                <el-col :xs="24" :sm="12" :md="8" :lg="6" :xl="6" v-for="(item,index) in website.list" :key="index" class="itemClass">
                    <a :href="item.url" class="tag">{{item.name}}</a>
                </el-col>
            </el-row>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        websiteOptions:{
            type:Object,
            default: function () {
                return { title: '前端导航', dataList: [] }
            }
        }
    },
    data () {
        return {
        };
    },

    mounted() {
        console.log(1111)
    },

    methods: {}
}

</script>
<style lang='scss' scoped>
.webSite{
    width:90%;
    margin: 30px auto;
    .listView{
        .listItem {
            box-sizing: border-box;
            box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
            padding: 0 20px;
            .itemClass{
                box-sizing: border-box;
                padding: 10px 10px;
                .tag{
                    width:100%;
                    display: inline-block;
                    height: 40px;
                    line-height: 40px;
                    text-align: center;
                    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.1);
                    &:hover{
                        background: #409eff;
                        color: #fff;
                    }
                }
            }
        }
        .HeadTitle{
            height: 40px;
            line-height: 40px;
            background: #409eff;
            color: #fff;
            padding: 0 25px;
        }
    }
}
</style>
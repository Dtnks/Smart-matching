<script lang="ts" setup>
import {ref} from "vue"
const current=ref("")
const desire=ref("")
let jdcontent=[{
    companyname:"公司名称",
    jdname:"职位名称",
    min:"最低薪资",
    max:"最高薪资",
},
{
    companyname:"公司1",
    jdname:"土建工程造价员",
    min:4000,
    max:8000,
},
{
    companyname:"公司2",
    jdname:"景观主创设计师",
    min:15000,
    max:25000,
},
{
    companyname:"公司3",
    jdname:"客服文员/网络客服",
    min:4000,
    max:8000,
},
{
    companyname:"公司4",
    jdname:"中安华筑技术标专员",
    min:4000,
    max:6000,
},
{
    companyname:"公司5",
    jdname:"项目拓展经理",
    min:10000,
    max:20000,
},
{
    companyname:"公司6",
    jdname:"厦门分行校园",
    min:10000,
    max:15000,
},
{
    companyname:"公司7",
    jdname:"会计",
    min:8000,
    max:5000,
},
{
    companyname:"公司8",
    jdname:"美容顾问",
    min:4000,
    max:8000,
},
{
    companyname:"公司9",
    jdname:"医学信息沟通专员",
    min:6000,
    max:8000,
}]

let option1=[
    {
        value:"房地产",
        label:"房地产"
    },
    {
        value:"建筑",
        label:"建筑"
    },
    {
        value:"建材",
        label:"建材"
    },
    {
        value:"工程",
        label:"工程"
    },
    {
        value:"工程造价",
        label:"工程造价"
    },
    {
        value:"预结算",
        label:"预结算"
    }
]
</script>
<template>
    <div id="app">
        <div id="form" class="row">
            <div class="col">    
                <p>目标城市</p>
                <input style="width: 240px;">
            </div>
            <div class="col">    
                <p>期望薪资范围</p>
                <div class="row">
                    <input style="width: 120px;" placeholder="最低">
                    <input style="width:120px" placeholder="最高">
                </div>
            </div>
            <div class="col">    
                <p>目前薪资范围</p>
                <div class="row">
                    <input style="width: 120px;" placeholder="最低">
                    <input style="width:120px" placeholder="最高">
                </div>
            </div>
            <div class="col">    
                <p>学历水平</p>
                <input style="width: 120px;">
            </div>
            <div class="col">    
                <p>年龄</p>
                <input style="width: 120px;">
            </div>
            <div class="col">    
                <p>工作开始时间</p>
                <input style="width: 120px;">
            </div>
            <div class="col" style="margin-right: 15px;margin-bottom: 30px;">    
                <p>希望的工作类型</p>
                <el-select
                v-model="desire"
                placeholder="Select"
                style="width: 320px;position: relative; top:15px;left:15px"
                clearable
                multiple
                size="large"
                >
                <el-option
                v-for="item in option1"
                :key="item.value"
                :label="item.label"
                :value="item.value"
                />
                </el-select>
            </div>
            <div class="col">    
                <p>目前工作的类型</p>
                <el-select
                v-model="current"
                placeholder="Select"
                style="width: 320px;position: relative; top:15px;left:15px"
                clearable
                multiple
                size="large"
                >
                <el-option
                v-for="item in option1"
                :key="item.value"
                :label="item.label"
                :value="item.value"
                />
                </el-select>
            </div>
            <div class="col">    
                <p>相关的工作经历</p>
                <input style="width:1200px">
            </div>
        </div>
        <div id="form" v-for="item in jdcontent">
            <div class="row tab" >
                <p>{{ item.companyname }}</p>
                <p>{{ item.jdname }}</p>
                <p>{{ item.min }}</p>
                <p>{{item.max}}</p>
            </div>

        </div>

    </div>
</template>
<style>
#form{
    margin:0 180px ;
    flex-wrap: wrap;
}
.col{
    display: flex;
    flex-direction: column;
}
.row{
    display: flex;
    flex-direction: row;
}
.col input{
    border: none;
    padding: 10px;
    background-color: #d6d6d6a9;
    border-radius: 5px;
    margin: 15px;
}
.input{
    border: none;
    padding: 10px;
    background-color: #d6d6d6a9;
    border-radius: 5px;
    margin: 15px;
}
.col p{
    margin: 0  0 0 15px;
}
.tab p{
    flex: 1;
    text-align: center;
}

</style>
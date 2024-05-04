<script lang="ts" setup>
import {ref} from "vue"
const current=ref("")
const desire=ref("")
const trelver=ref("")
let jdcontent=[{
    name:"姓名",
    age:"年龄",
    min:"最低薪资",
    max:"最高薪资",
    degree:"学历"
},
{
    name:"XXXXX",
    age:"23",
    min:4000,
    max:8000,
    degree:"本科"
},
{
    name:"XXXXX",
    age:"21",
    min:6000,
    max:8000,
    degree:"本科"
},
{
    name:"XXXXX",
    age:"23",
    min:8000,
    max:12000,
    degree:"本科"
},
{
    name:"XXXXX",
    age:"24",
    min:10000,
    max:15000,
    degree:"硕士"
},
]

</script>
<template>
    <div id="app">
        <div id="form" class="row">
            <div class="col">    
                <p>所在城市</p>
                <input style="width: 240px;">
            </div>
            <div class="col">    
                <p>工作岗位</p>
                <input style="width: 240px;">
            </div>
            <div class="col">    
                <p>薪资范围</p>
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
                <p>所需工作时间</p>
                <input style="width: 120px;">
            </div>
            <div class="col" style="margin-bottom: 30px;">    
                <p>出差需求</p>
                <el-select
                v-model="trelver"
                placeholder="Select"
                style="width: 320px;position: relative; top:15px;left:15px"
                clearable
                size="large"
                >
                <el-option
                v-for="item in [{value:'需要',label:'需要'},{value:'不需要',label:'不需要'}]"
                :key="item.value"
                :label="item.label"
                :value="item.value"
                />
                </el-select>
            </div>
            <div class="col">    
                <p>岗位描述</p>
                <textarea style="width:1200px;height: 80px;" type="text" class="input"></textarea>
            </div>
        </div>
        <div id="form" v-for="item in jdcontent">
            <div class="row tab" >
                <p>{{ item.name }}</p>
                <p>{{ item.age }}</p>
                <p>{{ item.min }}</p>
                <p>{{ item.max }}</p>
                <p>{{ item.degree }}</p>
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
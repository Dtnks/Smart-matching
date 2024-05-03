<template>
    <div id="app">
        <div class="content" >
            <img src="../image/微信图片_20240420171600.jpg" style="width: 40px;height: 40px;border-radius: 8px;">
            <div class="send">
                <div class="row"></div>
            </div>
        </div>
    </div>
</template>
<style>
.content{
    padding: 20px;
    position: relative;
    display: flex;
    flex-direction: row;
    background-color: rgba(153, 153, 153,0.5);
}
.send{
  width:150px;
  height:35px;
  background:#ffffff;
  border-radius:5px; /* 圆角 */
  margin: 0  0 0 20px;
}
 
.row {
    position: relative;
    top:9.5px;
    left:-16px; /* 圆角的位置需要细心调试哦 */
    width:0;
    height:0;
    font-size:0;
    border:solid 8px;
    border-color:transparent #ffffff transparent transparent;
}

</style>
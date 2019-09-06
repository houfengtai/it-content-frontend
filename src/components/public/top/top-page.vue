<template>
    <div class="top-page">
        <div class="top-content">
            <div class="web-logo">
                <img>
                <span>
                    <span class="size-big">IT</span><span class="size-normal">content.cn</span>
                </span>
            </div>
            <div class="top-nav">
                <ul>
                    <li class="li-checked"><div>首页</div><div></div></li>
                    <li><div>题海</div><div></div></li>
                    <li><div>话题</div><div></div></li>
                    <li><div>投票</div><div></div></li>
                    <li><div>关注</div><div></div></li>
                </ul>
            </div>
            <div class="top-user-info">
                欢迎【少年的你】 | 退出
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'top-page',
  props: ['selectIndex']
}
</script>

<style scoped>
.top-page{
    min-height:100px;
}
.top-content{
    width: 1200px;
    height:80px;
    margin: auto;
}
.top-nav{
    float:left;
    height: 40px;
    margin-top:20px;
}
.top-nav ul{
    list-style: none;
    margin: 0;
    padding: 0;
}
.top-nav ul li{
    display: inline-block;
    float:left;
    margin-right:20px;
    height:40px;
    line-height:40px;
    font-size:16px;
}
.top-nav ul li div:nth-child(2){
    height:2px;
    width:0px;
}
.top-nav ul li:hover{
    cursor: pointer;
    color: #00c1dc;
}
.top-nav ul li:hover div:nth-child(2){
    animation: nav-border-movie 0.3s ease-in-out 0s 1 alternate forwards;
}

.web-logo{
    width:200px;
    float:left;
    margin-top:20px;
    height: 40px;
}
.size-normal{
    font-size: 18px;
}
.size-big{
    font-size: 36px;
}
.top-user-info{
    float:right;
    height:40px;
    margin-top:20px;
    text-align: right;
    line-height:40px;
    font-size: 16px;
}
.top-nav ul li.li-checked{
    color: #00c1dc;
}
.top-nav ul li.li-checked div:nth-child(2){
    background:#00c1dc;width:100%;
}
@keyframes nav-border-movie {
    form {background:none;width: 0px;}
    to {background:#00c1dc;width:100%;}
}
</style>

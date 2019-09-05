<template>
    <div class="top-page">
        <div class="top-content">
            <div class="web-logo">
                <img>
                <span>
                    <span class="size-big">IT</span><span>content.cn</span>
                </span>
            </div>
            <div class="top-nav"></div>
            <div class="top-user-info"></div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'top-page'
}
</script>

<style scoped>
.top-page{
    min-height:100px;
}
.top-content{
    width: 1200px;
    border:1px solid red;
    height:80px;
    margin: auto;
}
    .size-big{
        font-size: 30px;
    }
</style>

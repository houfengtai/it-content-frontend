<template>
    <div class="index-page">
        <top-page></top-page>
        <div class="index-content"></div>
    </div>
</template>
<script>
import TopPage from '@/components/public/top/top-page'

export default {
  name: 'index-page',
  metaInfo: {
    title: '题海 itcontent.cn 一个帮助个人提高面试成功率的社区',
    meta: [{
      name: 'keywords',
      content: '题海,itcontent.cn,题海社区,在线学习,面试技巧,IT提升,自我提升'
    },
    {
      name: 'description',
      content: '【题海】专注于帮助个人提高面试成功率的社区。在线刷题交流，提问，吐槽，职业冷笑话等等尽在题海社区'
    }
    ]
  },
  components: { TopPage },
  data () {
    return {
      msg: '欢迎来到题海社区'
    }
  },
  methods: {

  },
  mounted () {

  }
}
</script>

<style scoped>
.index-page{
    min-height: 500px;
}
.index-content{
    width:1200px;
    height:780px;
    border:1px solid red;
    margin: auto;
}
</style>

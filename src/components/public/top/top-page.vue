<template>
    <div class="top-page">
        <div class="left-line-gradual"></div>
        <div class="top-content">
            <div class="web-logo">
                <img>
                <span>
                    <span class="size-big">IT</span><span class="size-normal">content.cn</span>
                </span>
            </div>
            <div class="top-nav">
                <ul>
                    <li v-for="nav in navs" :key="nav.id" :class="_selected(nav.name)"><div><a :href="nav.url">{{nav.label}}</a></div><div></div></li>
                </ul>
            </div>
            <div class="top-user-info">
                欢迎【少年的你】 | 退出
            </div>
        </div>
        <div class="right-line-gradual"></div>
    </div>
</template>

<script>
export default {
  name: 'top-page',
  props: ['selectIndex'],
  data () {
    return {
      navs: [
        {
          id: '1',
          name: 'index',
          label: '首页',
          url: '/index'
        },
        {
          id: '2',
          name: 'exam',
          label: '题海',
          url: '/exam'
        },
        {
          id: '3',
          name: 'topic',
          label: '话题',
          url: ''
        },
        {
          id: '4',
          name: 'vote',
          label: '投票',
          url: ''
        },
        {
          id: '5',
          name: 'focus',
          label: '关注',
          url: ''
        }
      ],
      userInfo: {
        userName: '张三',
        userImage: ''
      },
      isLogin: true
    }
  },
  methods: {
    _isShow () {
      let name = this.$route.name
      if (name === 'us') {
        return false
      }
      return true
    },
    _selected (name) {
      if (name === this.selectIndex) return 'selected'
      return ''
    },
    _getUserInfo () {
      let user = window.localStorage.getItem('userInfo')
      if (user == null || user === '' || user === '{}') {
        this.userInfo = {}
        this.isLogin = false
      } else {
        this.userInfo = JSON.parse(user)
        this.isLogin = true
      }
    }
  },
  mounted () {
    this._getUserInfo()
  }

}
</script>

<style lang="scss" scoped>
    @import "./assets/scss/top-page.scss";
</style>

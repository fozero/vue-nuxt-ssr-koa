<template>
<div class="container">
    <div class="main">
      <div class="menu clearfix">
        <div class="fl title">热门文章</div>
        <ul class="fl tabs">
          <li class="tab" :class="activeTab==1?'selected':''" @click="tab(1)">推荐</li>
          <li class="tab" :class="activeTab==2?'selected':''" @click="tab(2)">前端</li>
          <li class="tab" :class="activeTab==3?'selected':''" @click="tab(3)">Android</li>
          <li class="tab" :class="activeTab==4?'selected':''" @click="tab(4)">后端</li>
        </ul>
      </div>
      <ul class="contents">
        <li class="content">
          <div class="title">
            <div>
              专栏-fozero-3小时前-前端
            </div>
            <div>
              一个帮助开发者成长的社区
            </div>
            <div>
              喜欢234 评论224
            </div>
          </div>
          <div class="thematic">
            <img src="https://www.baidu.com/img/bd_logo1.png">
          </div>
          <div class="clearfix"></div>
        </li>
        <li class="content">
          <div class="title">
            <div>
              专栏-fozero-3小时前-前端
            </div>
            <div>
              一个帮助开发者成长的社区
            </div>
            <div>
              喜欢234 评论224
            </div>
          </div>
          <div class="thematic">
            <img src="https://www.baidu.com/img/bd_logo1.png">
          </div>
          <div class="clearfix"></div>
        </li>
        <li class="content">
          <div class="title">
            <div>
              专栏-fozero-3小时前-前端
            </div>
            <div>
              一个帮助开发者成长的社区
            </div>
            <div>
              喜欢234 评论224
            </div>
          </div>
          <div class="thematic">
            <img src="https://www.baidu.com/img/bd_logo1.png">
          </div>
          <div class="clearfix"></div>
        </li>
        <li class="content">
          <div class="title">
            <div>
              专栏-fozero-3小时前-前端
            </div>
            <div>
              一个帮助开发者成长的社区
            </div>
            <div>
              喜欢234 评论224
            </div>
          </div>
          <div class="thematic">
            <img src="https://www.baidu.com/img/bd_logo1.png">
          </div>
          <div class="clearfix"></div>
        </li>
      </ul>
    </div>
    <div class="side">
      <div class="login">
        <div>
          <b>掘金 - juejin.im</b><br/>
一个帮助开发者成长的社区
现在注册，送你45元买小册
        </div>
        <mu-text-field hintText="提示文字"/><br/>
        <mu-text-field hintText="提示文字"/><br/>
        <mu-text-field hintText="请输入密码" type="password"/><br/>
        <mu-raised-button label="Primary" class="demo-raised-button" primary/><br/>
      </div>
    </div>
    <div class="clearfix"></div>
  </div>
</template>

<script>
// import TopicListChalk from '~/components/TopicListChalk'
import api from '../static/js/api.js'

export default {
  // async asyncData ({}) {
  // 	return api.getLatestTopics()
  // 		.then((res)=>{
  // 			console.log(res)
  // 			return {list:res}
  // 		})
  // },
  data () {
    return {
      activeTab: '1'
    }
  },
  methods: {
    handleTabChange (val) {
      this.activeTab = val
    },
    handleActive () {
      window.alert('tab active')
    },
    tab(type){
      this.activeTab=type;
    }
  }



}
</script>

<style scoped>
*{
      padding: 0;
    margin: 0;
}
.container{width: 900px;margin:0 auto;}
.clearfix{clear: both;}
.main{float:left;background: #fff;width: 600px;margin-top: 40px;}
.side{float:left;background: #fff;width: 200px;margin-left: 20px;margin-top: 40px;}
.main .menu{
  padding: 20px 10px;
}
.main .menu .title{}
.tabs{
  list-style: none;
  border-bottom: 1px solid #eee;
}
.tabs .tab{
  display: inline-block;
  padding: 20px 10px;
}
.tabs .selected{
  color:#007fff;
}
.contents{
  list-style: none;
}
.contents .content{
  border-bottom: 1px solid #eee;
  padding: 20px;
}
.title{float:left;width: calc(100%-120px);margin-top: 20px;}
.thematic{float:left;width:120px;}
.thematic img{width:100px;height: 100px;}

.side .login{
  text-align: center;
    padding: 10px;
}
.side .login .mu-text-field{
  width: 150px;
}
</style>

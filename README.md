# vue-demo
## vue.js安装
国内下载的速度比较慢，可以使用代理或者其他的CDN方式进行下载
```
# 查看版本
npm -v
# 升级npm
cnpm install npm -g
# 升级或安装 cnpm
npm install cnpm -g
# 最新稳定版
$ cnpm install vue
# 全局安装命令行工具vue-cli
cnpm install --global vue-cli
# 创建一个基于webpack模版的新项目
vue init webpack my-project
# 进入安装目录
cd my-project
# 安装
cnpm install
# 运行
cnpm run dev
# 访问
http://localhost:8080
```
## vue.js起步
```
var vm = new Vue({
  el: '#app',
  data: {
    message: 'Tom!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```
## vue.js模版语法
- v-model
- v-bind
- v-if
- v-on
- 过滤器：
```
<div id="app">
  {{ message | capitalize }}
</div>
	
<script>
new Vue({
  el: '#app',
  data: {
	message: 'Lucy'
  },
  filters: {
    capitalize: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    }
  }
})
</script>
```
- 缩写形式：
- v-bind:href="url" == :href="url"
- v-on:click="doSomethings" == @click="doSomethings"


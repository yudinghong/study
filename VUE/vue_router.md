# vue-router 

在src目录下建立router.js文件对路由进行配置

```javascript
import Home from './pages/Home'

export default [
	{path: '', component: Home},
]

// or

export default [
	{path: '', component: ()=>{
		import('......')
	}}
]

```

其中每个对象都有属性如下：
```javascript
{
	path: '', // 路由
	name: '', // 别名
	component: '', //组件
	redirect: '' || {name: ''}, // 可以是路由字符串也可以是别名
	props: true || {default: true, }, // 路由最后加上参数比如 /index/:id  组件中通过props访问
	children: 
}

```
props一共三种模式
* 布尔模式：  
  如果 `props` 被设置为 `true`，`route.params` 将会被设置为组件属性

* 对象模式  
  如果 `props` 是一个对象，它会被按原样设置为组件属性。当 `props` 是静态的时候有用
	```javascript
	const router = new VueRouter({
		routes: [
			{ path: '/promotion/from-newsletter', component: Promotion, props: { newsletterPopup: false } }
		]
	})
	```

* 函数模式
  你可以创建一个函数返回 `props`。这样你便可以将参数转换成另一种类型，将静态值与基于路由的值结合等等
	```javascript
	const router = new VueRouter({
		routes: [
			{ path: '/search', component: SearchUser, props: (route) => ({ query: route.query.q }) }
		]
	})
	```

在main.js中

```javascript
import VueRouter from 'vue-router'
import routes from './router'

Vue.use(VueRouter)

var router = new VueRouter({
  mode: 'history',
  base: __dirname,
  routes,
})

export default new Vue({
  el: '#app',
  store,
  router,
  render: (h) => h(App),
})
```

## router-view

## vue router.beforeEach()

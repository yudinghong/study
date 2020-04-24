# axios 学习

## 使用方法

```
npm install vue-axios  
npm install qs.js --save　　//这一步可以先忽略，它的作用是能把json格式的直接转成data所需的格式
```

```javascript
import Vue from 'vue'  
import axios from 'axios'  
Vue.prototype.$axios = axios    //全局注册，使用方法为:this.$axios  
Vue.prototype.$qs = qs           //全局注册，使用方法为:this.qs  
```

```javascript
axios.interceptors.request.use(config=>{
	// config.headers 请求头

},err=>{

})

axios.interceptors.reponse.use(response=>{
	// config.headers 请求头
	
},err=>{

})
```
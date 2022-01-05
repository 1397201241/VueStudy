#### 记录学习过程中遇到的问题

1. Vue实例方法methods和计算属性computed不能同名（会导致后者无效）

2. 区别声明式渲染和命令式渲染？
   　　命令式：需要以具体代码表达在哪里做什么？它是如何实现的
      　　声明式：只需要声明在哪里需要做什么？不需要关心具体怎么实现的

   实例：（假设有一个数组，我们要让里面的每个数字乘以2）

   　　命令式：

   ```javascript
   let arr=[2,4,5,6]
   let arr2=[]
   for(let i=0;i<arr.length;i++){
       arr2.push(arr[i]*2)
   }
   ```

   　声明式：

   ```javascript
   let arr=[2,4,5,6]
   let arr2=arr.map(item=>item*2)
   console.log(arr2)
   ```

3. vue-cli各版本的挂载（混合报错）

     vue3:

     ```javascript
     createApp(App).mount('#app')*/
     import { createApp } from 'vue'
     import App from './App.vue'
     import router from './router'
     import store from './store'
     
     const app = createApp(App)
     app.use(store)
     app.use(router)
     app.mount('#app')
     ```

     vue2:

     ```javascript
     import Vue from 'vue'
     import App from './App'
     import router from './router'
     
     Vue.config.productionTip = false
     
     /* eslint-disable no-new */
     new Vue({
         el: '#app',
         router,
         render: h => h(App)
     })
     /*
     new Vue({
         router,
         render: h => h(App)
     }).$mount('#app')
     */
     ```

4. 在<style>里定义的样式加上scoped属性时，自定义样式无法生效，去掉后又可以（scoped属性表示样式作用于当下模块）

5. s




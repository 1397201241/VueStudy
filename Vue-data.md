#### Vue的data

1. data为什么要这样写

   ```javascript
   data() {
     return {
       message: 'good good study'
     }
   },
   ```

   很多情况下，组件会在很多地方被调用，因此，为了保证数据的独立性，通过匿名函数返回一个具有局部作用域的data对象，防止全局污染。

2. data中使用`Object.freeze()`的目的

   ```vue
   <el-table v-bind="cellStyle">
   </el-table>
   ```

   ```javascript
   data() {
     return {
       cellStyle: Object.freeze({
         color: '#fff'
       })
     }
   }
   ```

   冻结静态状态，不进行`diff`算法，提升性能

3. coming...






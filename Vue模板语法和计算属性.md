#### Vue模板语法

##### 插值

数据绑定的最常见形式是使用“Mustache”语法（双大括号）的文本插值

```html
<p>{{message1}}</p>
```

##### 指令

指令是指带有"v-"前缀的特殊attribute，例如"v-bind",一般是单个JavaScript表达式（v-for除外）

#### 计算属性和侦听器

##### 计算属性

在声明Vue实例时可以通过computed定义计算属性，简化模板逻辑（从视图层转移到定义上）

```html
<p>{{message1.split('').reverse().join('')}}</p>
```

例如上面的这个字符串反转的逻辑可以通过computed转移到Vue实例的定义上

```javascript
//声明计算属性
computed:{
    reverseMessage1:function () {
        return this.message1.split('').reverse().join('');
    }
}
```

注意，虽然看起来这和定义方法达到一样的效果，但是计算属性是**基于响应式依赖进行缓存**的，也就是只有message1改变了才会进行重新计算，不然都是返回前一次的结果，而每次调用methods里的方法的话都会执行一次函数。


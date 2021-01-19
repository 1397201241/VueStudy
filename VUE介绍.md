#### 引入

```html
<!--引入VUE-->
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.12"></script>
```

#### 声明式渲染

vue.js可以声明式得将数据渲染到DOM系统，例如

声明一个ID为"#app"的元素

```javascript
var app=new Vue({
    el:'#app',
    data:{
        message:'hello world!'
    }
});
```

```html
<div id="app">
    {{message}}
</div>
```

[helloworld.png](https://github.com/1397201241/img/blob/main/helloworld.png)

v-bind绑定元素属性，例如

```javascript
var app2=new Vue({
    el:'#app2',
    data:{
        message:new Date().toUTCString(),
    }
})
```

```html
<div id="app2">
    <!--v-bind可用于绑定元素属性-->
    <span v-bind:title="message">
        悬停几秒可查看元素提示信息
    </span>
</div>
```

[v-bind.png](https://github.com/1397201241/img/blob/main/v-bind.png)

#### 条件与循环

v-if绑定条件，v-for绑定数组的数据

```javascript
var app2=new Vue({
    el:'#app2',
    data:{
        todos:[
            {text:'react'},
            {text: 'vue'}
        ],
        message:new Date().toUTCString(),
        flag:true
    }
})
```

```html
<div id="app2">
    <!--v-bind可用于绑定元素属性-->
    <span v-bind:title="message">
        悬停几秒可查看元素提示信息
    </span>
    <p v-if="flag">you can see me</p>
    <ol>
        <li v-for="todo in todos">
            {{todo.text}}
        </li>
    </ol>
</div>
```

[v-if_v-for.png](https://github.com/1397201241/img/blob/main/v-if_v-for.png)
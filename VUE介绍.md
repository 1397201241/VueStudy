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

![helloworld.png](https://github.com/1397201241/img/blob/main/helloworld.png?raw=true)

**v-bind**绑定元素属性，例如

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

![v-bind.png](https://github.com/1397201241/img/blob/main/v-bind.png?raw=true)

#### 条件与循环

**v-if**绑定条件，**v-for**绑定数组的数据

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

)

![v-if_v-for.png](https://github.com/1397201241/img/blob/main/v-if_v-for.png?raw=true)

#### 处理用户输入

**v-on:click**可以响应用户点击事件

```javascript
//声明方法
methods:{
    reverseMessage:function () {
        this.message1=this.message1.split('').reverse().join('');
    }
}
```

```html
<div>
    <p>{{message1}}</p>
    <button v-on:click="reverseMessage">
        反转消息
    </button>
</div>
```

![v-on.png](https://github.com/1397201241/img/blob/main/v-on.png?raw=true)
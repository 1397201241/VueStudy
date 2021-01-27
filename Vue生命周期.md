### Vue生命周期

每个Vue实例从创建到销毁经历四个阶段，即

*创建*

```javascript
beforeCreate:function(){
  console.log("VUE实例创建前，")
},
created:function(){
    console.log("Vue实例已创建。")
},
```

*挂载*

```javascript
beforeMount:function(){
    console.log("VUE实例挂载前，")
},
mounted:function(){
    console.log("Vue实例已挂载。")
},
```

*更新*

```javascript
beforeUpdate:function(){
    console.log("VUE实例数据更新前，")
},
updated:function(){
    console.log("Vue实例数据已更新。"+this.message1)
},
```

*销毁*

```javascript
beforeDestroy:function(){
    console.log("VUE实例销毁前，")
},
destroyed:function(){
    console.log("Vue实例已销毁。")
},
```
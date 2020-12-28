# js调试工具

### alert打印--不建议使用
    alert打印只能打印出字符串，如果打印的对象不是String,则会调用toString()方法将该对象转成字符串，比如转成 [object Object]这种
    alert会阻塞UI和javascript的执行，必须点击'OK'按钮才能继续，非常低效。
### console.log() 
存在打印出来是空数组点击展开之后有值的情况
解决方法：
```
this.$nextTick(()=>{
    console.log(arr, '打印空值，展开有值')
})
or
setTimeOut(()=>{
    console.log(arr, '打印空值，展开有值')
})
```

### console.dir():看一个DOM对象里面到底有什么属性和方法
    常规的 console.log打印出来的只是HTML标签
    如果我们想看到DOM对象作为JavaScript对象的结构可以使用 console.dir
    console.dir(document.getElementByClassName('divName'))
    console.dir可以打印出任何JavaScript对象的属性列表

### console.table()可以查看一个列表的多个属性中，单独的几个属性
    console.table(user, ['id','name','time'])
    
### console.time（） 和console.timeEnd()计算方法运行的时间

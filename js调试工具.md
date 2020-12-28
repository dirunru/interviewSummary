# js调试工具

### alert打印--不建议使用
    alert打印只能打印出字符串，如果打印的对象不是String,则会调用toString()方法将该对象转成字符串，比如转成 [object Object]这种
    alert会阻塞UI和javascript的执行，必须点击'OK'按钮才能继续，非常低效。
### console.log() 
存在打印出来是空数组点击展开之后有值的情况
```
this.$nextTick(()=>{
    console.log(arr, '打印空值，展开有值')
})
```

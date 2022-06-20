---
date created: 2022-06-20 15:18
date updated: 2022-06-20 15:46
---

- 延时函数 sleep()

```js
const sleep = (time) => {    
	const startTime = new Date().getTime() + parseInt(time, 10)  
	while(new Date().getTime() < startTime) {} 
} 
sleep(1000)
```

- 浏览器延时debug

```js
setTimeout(function(){debugger},3000)
```

- 计算函数执行时间

```js
console.time() 
console.timeEnd()
```

- 生成UUID

```js
URL.createObjectURL(new Blob()).substr(-36)
```

- 更好的typeof

```js
const typeOf = (obj) => {    
	return Object.prototype.toString.call(obj).slice(8, -1).toLowerCase() 
} 
typeOf([]) // 'array' 
typeOf({}) // 'object' 
typeOf(new Date) // 'date'
```

- 格式化字节大小

```js
const formatBytes = (bytes) => {  
	if (bytes == 0) return '0 Bytes'
	var k = 1024,     
	// dm = decimals || 2,    
	dm = 2,     
	sizes = ['Bytes', 'KB', 'MB', 'GB', 'TB', 'PB', 'EB', 'ZB', 'YB'],    
	i = Math.floor(Math.log(bytes) / Math.log(k));  
	return parseFloat((bytes / Math.pow(k, i)).toFixed(dm)) + ' ' + sizes[i]; 
}
```

- 打开新页面

```js
self.location.href;//当前页面打开URL页面 
window.location.href;//当前页面打开URL页面 
this.location.href;//当前页面打开URL页面 
location.href;// 当前页面打开URL页面 
parent.location.href;//在父页面打开新页面 
top.location.href;//在顶层页面打开新页面
```

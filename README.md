# yidaRule
```app目前已支持[漫画][音频][视频]```

```js规则与益达版亦搜类似；js调用部分函数不需要使用异步```


### 全局变量:

```
// 上一级的结果
result

// 规则基本信息,如host,httpHeaders
config

// params是一个解析基本变量,主要保存上级解析信息和一些变量

params.keyWord
params.pageIndex

// 更多键过滤器
params.filters

// 发现页tab索引;后续版本将每个分类单独处理,待删除的
params.tabIndex

```





### tools方法:
```
// 发送http请求
tools.httpRequest()
tools.http.post(url,body,headers)
tools.http.get(url,headers)
tools.rsaEncrypt(str,key)
tools.rsaEncryptWithPrivate(str,key)
tools.rsaDecryptWithPublic(str,key)

// 1.0.6≥版本生效
console.log([...])
console.warn([...])
console.error([...])

```

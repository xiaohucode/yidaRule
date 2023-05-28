# yidaRule
打包了个安卓版本,可在Windows11子系统中运行写规则

安装包获取:https://github.com/xiaohucode/yidaRule/releases


```app目前已支持[漫画][音频][视频][RSS]```

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

// 发现页tab索引;最新版本已删除,已无意义
params.tabIndex

```

### 规则内置CryptoJS,可直接使用

### tools方法:
```
// 发送http请求
tools.httpRequest()
tools.http.post(url,body,headers)
tools.http.get(url,headers)
tools.rsaEncrypt(str,key)
tools.rsaDecrypt(str,key)
tools.rsaEncryptWithPrivate(str,key)
tools.rsaDecryptWithPublic(str,key)

// CryptoJS 封装方法
md5Encode: (str) => CryptoJS.MD5(str).toString().toLowerCase(),
base64Encode: (str) => CryptoJS.enc.Base64.stringify(CryptoJS.enc.Utf8.parse(str)),
base64Decode: (str) => CryptoJS.enc.Base64.parse(str).toString(CryptoJS.enc.Utf8),
sha1Encode: (str) => CryptoJS.SHA1(str).toString(),
sha224Encode: (str) => CryptoJS.SHA224(str).toString(),
sha256Encode: (str) => CryptoJS.SHA256(str).toString(),
sha348Encode: (str) => CryptoJS.SHA384(str).toString(),
sha512Encode: (str) => CryptoJS.SHA512(str).toString(),
ripemd160Encode: (str) => CryptoJS.RIPEMD160(str).toString(),
// 调用方法
let res = tools.md5Encode('MD5');
console.log(res);


// 1.0.6≥版本生效
console.log([...])
console.warn([...])
console.error([...])

```

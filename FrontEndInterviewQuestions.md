 # General Front End Interview Questions

# 

### General

+ http://www.1point3acres.com/bbs/thread-104335-1-1.html
+ https://github.com/markyun/My-blog/tree/master/Front-end-Developer-Questions/Questions-and-Answers
    
    
HTML

+ 為何script要擺在body底端而非head底端？
```
因為讓網頁先load先呈現
```
+ Block Element, Inline Element
```
區分：開Inspector檢查，佔一整塊為block，小部分可卡進block區域的為Inline.
```
+ Div, Span Element
```
Div用作Grouping（沒有明確意義的Element）, 配合CSS做Styling展示小區塊的模式
Div : Block
Span : Inline
```
+ HTML5 Web Storage

```
localStorage.setItem('key', 'item')
let item = localStorage.getItem('key')
localStorage.removeItem('key')
```



ES6 Promise
+ 用於處理Asychronized, 讓Handler可以寫在多處(OOP)

```
向Http發出要求
GET request
axios.get('url').then(res => {
    res.status  // http response code
    res.data    // object parse by http body
    res.headers // http response header
}).catch(err =>{
    console.log(err)
})

POST request
axios.post('url', {
    //request body
}).then().catch()

* Request可被Cancel(ComponentWillOnMount)
GET, POST, PUT, DELETE
```

### React
+ Virtual DOM
    + 可以比較Virtual DOM跟Real DOM, 找出不同地方Re-render即可。用Reactstrap，因為Bootstrap底層用jQery寫的，會直接略過React的VirtualDOM特性。
+ Debugging
    + Babel compile可見語法錯誤
    + React Dev Tools Chrome Plugin, debugger;設斷點
    + propType用來做TypeChecking
    + bundle.js中的Dev tool: source-map可顯示未bundle前實際code出錯的片段, eval(build快，看不到原本code) --> source-map
    (build慢，但可見原code)

### State Management, Redux


1. From  URL to Web page
    + https://www.youtube.com/watch?v=ThSBPEza84A&list=PLlPcwHqLqJDlD86V7FNTP8d7JBvQmITrP
2. GET, POST Difference
    + http://www.webpage.idv.tw/study/03/09/method.htm

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
    + Specific to Domain(8080 port) and protocol(http/ https)
    + total > 5MB, 相同Domain & protocol可Share
    + value == Strings, 用JSON.stringify()或JSON.parse()來分析Object
    + sessionStorage在Window關掉後清空資料(打開一個Browser到關掉叫Session)
```
localStorage.setItem('key', 'item')
let item = localStorage.getItem('key')
localStorage.removeItem('key')
```
### Thinking In React
1. Identify Components and Props
2. Identify States (What might change during different time, find the common ancestor)
3. Identify Callbacks (第二是由上往下，此步由下往上)

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

### State Management Redux
+ Why Redux?
    1. 最上層的共同祖先要處理很多不同事物，程式邏輯發散
    + 更動UI時，移動component時要處理層層Callback的dataflow, 維護不易
    + States四散在不同的Component, 管理不易
    + 管理State與Rendering Logic結合，不合軟工分工角度
    + States Changes are implicit，因結合在Component裡，從何時開始跳轉與錯誤不易追蹤
    + Code for 'States' not code for 'changes'，UI的顯示與現在的State有關，而非凌亂的寫querySelect('div').style..
    + Virtual DOM track changes automatically
    + UI = maps from states to visual looks – Each component is a function of partial states 紀錄State而非如何差異（如何跳轉）
+ What is Redux?
    + State management framework
        + restrict how you write state management code
    + React(UI Rendering) + Redux(State Management, State Store)
    
```
render(){
    return ({
        <h1 className={this.state.toggle}> Hello {this.props.name}
        </h1>
    });
}
```    


1. From  URL to Web page
    + https://www.youtube.com/watch?v=ThSBPEza84A&list=PLlPcwHqLqJDlD86V7FNTP8d7JBvQmITrP
2. GET, POST Difference
    + http://www.webpage.idv.tw/study/03/09/method.htm

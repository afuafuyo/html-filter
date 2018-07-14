### html 过滤库 A library for filtering HTML tags and attributes written in JavaScript

###### demo

```
var html =
`
<div style="border: 1px solid red">
    <h1>Hello</h1>
    <div id="user" onclick="alert(1)">
        <p>zhangsan</p>
        <p>male</p>
        <p>20</p>
    </div>
</div>
`;

// 过滤标签和属性 filter tags & attributes
var obj = new XHtml();
obj.allowedTags = {div: true, p: true};
obj.allowedAttributes = {id: true, style: true};
obj.parse(html);

document.getElementById('container').innerHTML = obj.getHtml();
```
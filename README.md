# dlxpzh_test
简单使用git和github来管理自己的代码及笔记 https://my.oschina.net/bxxfighting/blog/378196

面试题 ： https://juejin.im/post/5aae076d6fb9a028cc6100a9

浏览器调试：
mqq-ios：
Mozilla/5.0 (iPhone; CPU iPhone OS 9_3_2 like Mac OS X) AppleWebKit/601.1.46 (KHTML, like Gecko) Mobile/13F69 QQ/6.3.5.437 V1_IPH_SQ_6.3.5_1_APP_A Pixel/750 Core/UIWebView NetType/WIFI Mem/96

mqq-android：
Mozilla/5.0 (Linux; Android 5.1.1; OPPO R7sm Build/LMY47V) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/37.0.0.0 Mobile MQQBrowser/6.8 TBS/036824 Safari/537.36 V1_AND_SQ_6.5.5_410_YYB_D PA QQ/6.5.5.2880 NetType/WIFI WebP/0.3.0 Pixel/1080


## css技巧
1：最后一个li去掉边框
.nav li:not(:last-child) {
  border-right: 1px solid #666;
}

2：垂直居中任何元素
html, body {
  height: 100%;
  margin: 0;
}

body {
  -webkit-align-items: center;  
  -ms-flex-align: center;  
  align-items: center;
  display: -webkit-flex;
  display: flex;
}

3：使列表的每项都由逗号分隔
ul > li:not(:last-child)::after {
  content: ",";
}

4：通用选择器 (*) 和 相邻兄弟选择器 (+) 一起使用，文档流中的所有的相邻兄弟元素将都将设置 margin-top: 1.5em 的样式
* + * {
  margin-top: 1.5em;
}

## js方法
1：判断类型
### typeof、instanceof、Object,prototype.toString.call()、constructor
let type = function(o) {
    let s = Object.prototype.toString.call(o);
    return s.match(/[object (.*?)]/)[1].toLowerCase();
};
console.log(type(12)) // number
console.log(type('12')) // string

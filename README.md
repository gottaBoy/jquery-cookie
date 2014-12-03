#jQuery Cookie

jQuery Cookie操作

##需求背景

在原生的JavaScript语句中，我们可以通过下面的两个属性获取Cookie的相关内容：

1. `navigator.cookieEnabled`
<br>该属性返回当前浏览器是否支持cookie操作。（返回类型：Boolean）
<br>目前而言几乎绝大多数浏览器都支持Cookie，只有那些有特殊需求的用户才会去禁用浏览器的Cookie。如果相关应用需要使用到cookie功能，请务必确保浏览器是否支持Cookie操作，否则应不给于处理。

2. `document.cookie`
<br>该属性是浏览器提供给开发人员管理当前域下的所有cookie的唯一途径（该属性可读写）。
<br>对该属性进行读操作，可以获取已有的所有cookie所组成的字符串内容。
<br>对该属性进行写操作，则可以添加cookie或者对cookie进行重新赋值。

代码实例：

```js

//写入cookie
document.cookie = "name=Jerry Sun";
document.cookie = "sex=male";

//取得cookie字符串
var str = document.cookie; //=> "name=Jerry Sun; sex=male"

```

原生操作并不能满足快速创建、编辑、移除某个cookie的需求，因此我们围绕这三点对Cookie操作进行了补充完善，从而构成了现在你所看到的jQuery Cookie插件。希望它能够帮助你快速编辑Cookie。

##使用jQuery Cookie插件

###获取Cookie

```js

$.cookie("name"); //=> "Jerry Sun"
$.cookie("sex");  //=> "male"

```

###创建/编辑Cookie

```js

$.cookie("name", "Jerry Sun");
$.cookie("sex", "male");

```

###移除Cookie

```js

$.cookie("name", null);
$.cookie("sex", null);

```
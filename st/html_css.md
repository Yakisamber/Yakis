##知识点

1. 前端 html css js/jquery
2. 数据库  sql查询
3. spring spintboot mybatis框架

一、 前端脚本

​	**html** ：	标签库	页面设置性标签

​	**css **：	重叠样式表	设置显示效果、位置控制

​	**js** ：	javascript 脚本语言 处理交互	BOM、DOM

### Html

```html
<!DOCTYPE html> // 通知浏览器页面版本 h5
<html>
<head> //非可视 设置

</head>
<body> //可视
    <a href="" target="_new"> name </a>
	<img alt="faultShow" src="a.jpg" width='100' height="200">
    <br> //换行
    <p> 段落 </p>
    <span> 行内布局容器 行 </span>
    
    <div>
        快内布局容器 列
    </div>
    
    <form action="b.jsp" method="get"> //目标地址 请求类型
       <input type="text" name=as value="123">
		<input type="hidden" name="asd" value="asd"> 
		
		<input type="checkbox"> 
		<br>
		
		<input type="radio" name="n1" value="0">a
		<input type="radio" name="n1" value="1">b
        //name需要一样
		
		<br>
		
		<select>
			<option value="0">男</option>
			<option value="1">女</option>
		</select>
	</form>
	
	<table>
	<tr><td> 1 </td> <td> 2 </td> 
	<tr><td> 1 </td> <td> 2 </td> 
	<tr><td> 1 </td> <td> 2 </td> 
	</table>
	
</body>
</html>
```

![1550214523795](C:\Users\69480\AppData\Roaming\Typora\typora-user-images\1550214523795.png)

#### 请求类型：

get ： url地址完成请求全部内容

post： url独立，内容在协议请求内

#### 按钮：

submit ：提交  reset ：清空表单  button ：普通按钮

### CSS

1. 使用方法

   * 使用style属性  	适用于特例 测试
   * 使用 `<style>`标签 	 适用于当前页特有样式 

   * `<link href="testCSS.css" rel="stylesheet">` 适用于 （整个站）通用型样式  皮肤功能

     

2. 选择器

3. 属性

####使用方法

```html
<head>  
	<style type="text/css">
		a{	 //标签选择器 当前页面所有标签
			color: #ee0000;font-size: 30px;
		}
        #name{	//id选择器 
			color: red;
		}
        .back{	//类选择器 class属性可指定多各类 
			background-color: yellow;
		}
        [name=sex1]{ 	//属性选择器  值为中文或数字 需加''单引号
			background-color: yellow;
		}
        #name,.s50{	//或选择器 
			color: red;
		}
        form select{ 	//子孙选择器 级数无限
			color: bule;
		}
        form>select {//子孙选择器 级数仅一级
			color: bule;
		}
	</style>
</head>

<a href="" target="" style=" color: #ee0000;font-size: 30px;"> name </a>
<input type="text" name=as value="123" class="back">

```

**优先级 ** ： 自上向下  选择范围越大 优先级越小

**重叠样式**  ： 相同属性在同标签实现，按优先级覆盖

```html
<head>
	<link href="testCSS.css" rel="stylesheet">
</head>
```

##### 大小 定位

* width height ( 100px  50% 根据上级容器限定)
* left right bottom top ( 100px 50% position 属性 设定定位方式)  **运算符前后加空格**
  * position 定位方式
  * margin 外边距       **占位偏移** 适合微调   (参数可为 $0$ )
  * padding 内边距    内部挤压显示部分 若未设定宽度 则大小改变
  * border 边框      
*  超级绝对定位 `position:fixed` （以左上角为 $(0,0)$  单独成为一层 脱离）
* 绝对定位`position:absolute` ( 以上级左上角为$(0,0)$ )
* 相对定位 `position:relative` (原 未设置定位时的 默认位置的 偏移量)

## Java

#### Java ee 

**web机制** 

1. web服务器 （指定到应用程序，加入http 协议解析）
2. 应用程序解析URL请求信息，找到目标处理程序（代码段）
3. 代码段接受请求对象（ 浏览器发出  get 、 post） 
4. 根据请求信息处理业务（ 数据库 ）
5. 业务结果处理（页面渲染，填充html 数据 ）
6. 将结果写入回应对象( 输出流 )
7. 浏览器解析http数据
8. 浏览器显示

******

### jsp

`<% java代码 %>` 写代码

`<%= 变量 >` 

### servlet

1. 创建类 继承httpservlet 重写doget方法

#### 转发

1. 地址转发 

   * 地址转换（ 一个新请求 ）

   url地址修改 回车

   `<a>` 标签点击

   `<form>` 请求

   js ` location.href='edit.jsp'` 

   

2. 请求转发( 可以中途添加数据)

   * 地址不更换  请求接力



#### view（全面替代jsp脚本）

jstl java标准标签库  `c:if` `c:foreach`

el:    数据获取表达式 `${list}` `${requestScope.list}`     	

> *不报错（独立的异常处理）* 
>
> 直接调用get方法 ，没有则直接报错

******

![img](file:///C:\Users\69480\Documents\Tencent Files\694808829\Image\C2C\6Z[LQ%P`@B]3SMP87SI]1OL.png)

2.  
   1. 创建servlet （类	web.xml 	指定地址访问类)
   2. 方法入口  doge  dopost
   3. 请求参数处理 （业务入口  需求决定）、
   4. 处理业务（变化前后的区别）
   5. 数据返回
      * response.getwriter (输出不能多 ，麻烦)
      * 请求转发（视图模板填充数据）



*****

404 地址与目标程序不一致  核对路径

* url地址 	web.xml 地址冲突问题	地址`/` 	post get dopost(405)  		运行方法错误

500  服务端代码错误 （ 运行Java代码时发生异常）

* 自上向下查看错误信息 找第一个用户代码行 点击 跳转到错误行（详看异常信息）
  * nullpoint exception 	调用null对象的属性或方法
  * indexoutbound exception  索引超出范围

#### 运行方法

关闭之前程序

通过点击项目右键菜单运行 （jsp页面修改不需要重新运行）

关闭其他项目

清空servers的发布目录

情况word路径 （jsp class 工具类）

清空project-clean （开发工具缓存）


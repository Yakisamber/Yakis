## mybatis(ORM框架-对象关系映射)

#### 安装设置

1. 库导入

   ```html
   <dependency>
   			<groupId>mysql</groupId>
   			<artifactId>mysql-connector-java</artifactId>
   			<version>5.1.47</version>
   		</dependency>
   		
   		<dependency>
               <groupId>org.mybatis.spring.boot</groupId>
               <artifactId>mybatis-spring-boot-starter</artifactId>
               <version>1.3.1</version>
           </dependency>
   ```

2.  数据连接设置

   ```
   spring.datasource.driver-class-name=com.mysql.jdbc.Driver
   spring.datasource.url=jdbc:mysql://localhost:3306/dz190216?useUnicode=true&characterEncoding=UTF-8&useSSL=true
   spring.datasource.username=root
   spring.datasource.password=lmz52531
   ```

3. 创建dao、接口，必须@Repository， 方法要注解

4. 设置启动类，@MapperScan（“com.example.demo.dao”）

5. 创建service接口 （大部分与mapper接口一致）

6. 创建serviceImpl 实体 引用对应service接口 必须@Servlet 必须@Autowired mapper实例用于数据库处理

7. 创建控制器类，@controller必须@Autowired service实例哦那个与数据库处理
       （使用接口的意义：减少耦合度，aop代理支持）



### MVC

* VIEW ：b.html
* controller： testController
* model： 业务模板    service serviceImpl
* 底层数据：entity（model）   mapper（数据库处理）

* 设置： application.properties  一次成型
* 启动文件： DemoApplication  一次成型

****

**VIEW**: b.html (发送请求)

​	url重定向请求 （get） 

1. 输入地址回车

   2. <a href=""> 点击

   3. <button onclick="location.href='地址'"> 点击

      form表单请求 （输入信息进行发出请求）

      ​	<form methon='get/post'> submit提交

      请求本质： 浏览器（客户端）自身不能解决的，从服务端处理获取的手段

###### controller： testController

​	内容 ：行为（客户端行为）
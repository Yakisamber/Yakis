## spring boot

1. 目录结构 

   src\main\java  	文件夹 java代码

   src\main\resources 	配置文件、view文件、静态资源文件（css，js，pic）

   src\test\java		测试用例

   pom.xml		配置文件

   target 			目标文件，无人工参与

2. maven   构建框架
   仓库 ：公共仓库、私服仓库、私人仓库（用户文件夹/.m2)

3. anotation： 注解  （标注方法、变量、类）
    `@RestController` 类 （类为控制器）



![th](D:\StudySoftware\TyporaSave\st\th.png)

*****

****

3. 取值  

   if

   ```html
   <li th:if="${#object.type==1}">admin管理员</li>
   <li th:if="${#object.type eq 2}">admin管理员</li>
   <li th:if="${#object.type} eq 1">admin管理员</li>
   <li th:if="${#object.type} == 2s">admin管理员</li>
   ```

   foreach

   ```html
   <tr th:each="user:${userlist}">
       <td th:texe="%{user.type}"></td>
   </tr>
   <tr th:each="user,userStat:${userlist}" th:class="${userStat.odd}?'odd':'even'"></tr>
   ```

   



1. 当前迭代索引从0开始，     索引属性 index
2. 当前迭代索引，从0开始     统计属性 count
3. 元素的总量迭代变量           大小属性size
4. iter变量为每个迭代             目前的财产current
5. 是否当前迭代是奇数还是偶数 even/odd 的布尔属性
6. 是否第一个当前迭代          first布尔属性
7. 是否最后一个当前迭代      last不二属性


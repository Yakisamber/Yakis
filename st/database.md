## 数据库

### 创建表

> 基本不为空

id 列 int 不为空 主键 自动编号

字符类型

* varchar 定长 、

* text 不定长

类型不能直接文本

date 类型可用字符串代替

*******

`insert into` 表名 （列名 ，...) value( 值，...)  增加一条记录（ 可省列，自动编号，有默认值，可为null ）

`update` 表名 set 列名 = 值，... [where 条件]  	修改指定记录（列根据需要设， 条件可选但通常要加）**单表更新**

delete from 表名 [where 条件] 				删除指定记录 **单表删除 **

select [ distinct ] [ * | 列名 [ 别名 ] ,...] from [ 表名 [ inner | right | left ] join 表名 on 关系条件 ] [ where 多表条件 and | 其他条件 ] [ group by 别名 ，...] [having 聚合条件 and | or...] [order by 别名，...] [limit...]

 ```mysql
SELECT name `name`,sex from `use`
where name like `%x%` # 模糊查询
 ```

#### 表关系

* 一对一    扩展表关系
* 多对多    学生与课程 （ 关联中间表 ）
* 一对多    业务单据主要明细表 整套数据 不独立存在 数据间有运算依赖
* 多对一    一方对多方的信息补充  （ 班级学生 ）

```mysql
//内联查询
SELECT `user`.* ,class.name classname
from `user` INNER JOIN class on `user`.classid=class.classid
```

```mysql
//外联查询 （不允许）
SELECT `user`.* ,class.name classname
from `user` ,class where `user`.classid=class.classid
```

`limit 5 ` 只查询制定数量记录

`limit  2 5 ` 从第二条记录开始 读取5条

 实现换页操作


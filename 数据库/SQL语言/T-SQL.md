变量
- 局部变量：变量名前加1个@符号
- 全局变量：变量名前加2个@@符号。如:
	- @@ERROR：当事务成功时为0，否则为最近一次的错误号
	- @@ROWCOUNT：返回受上一语句影响的行数
	- @@FETCH_STATUS：返回最近的FETCH语句执行后的游标状态
变量的声明与赋值
- 声明变量的语法
```sql server
DECLARE <@variableName> <datatype> [, <@variableName> <datatype> … ]
```
- 单个变量赋值的语法
```mysql
SET <@variableName> = <expr>
```
- 变量列表赋值(或显示表达式的值)的语法
```mysql
 SELECT <@variableName> [= <expr | columnName>]
	[, <@variableName> [= <expr | columnName>] … ]
```
运算符
函数
流程控制语句
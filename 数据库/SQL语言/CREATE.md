```mysql
CREATE DATABASE <databaseName>

[ ON [PRIMARY] { <filespec> [, ... n ] } ]

         [, { FILEGROUP <filegroupName> {<filespec> [, ... n ]} [, ... n ]} ] ]

[ LOG ON { <filespec> [, ... n ] } ] 
```
- \<databaseName\>
	- 被创建数据库的名字，满足如下要求
		- 长度从1到30，第一个字符必须是字母，或下划线_，或字符@
		- 在首字符后的字符可以是字母、数字或者前面规则中提到的字符
		- 名称中不能有空格
		- 数据库的大小可以被扩展或者收缩

![[Pasted image 20221223232404.png]]

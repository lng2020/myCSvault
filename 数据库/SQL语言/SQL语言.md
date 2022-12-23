查询
```mysql
SELECT …  FROM …  [WHERE … ] [GROUP BY …  [HAVING … ]]  [ORDER BY … ]
```
定义
```mysql
CREATE/ALTER/DROP   DATABASE/TABLE/VIEW/INDEX
```
修改
```mysql
INSERT/DELETE/UPDATE
```
游标
```mysql
DECLARE <cursorName> CURSOR FOR <SQL-Statements> [ FOR … ]
```
存储结构
```mysql
CREATE PROCEDURE <procName>(<@paraName> <datatype>) AS <SQL-Statements>
```
触发器
```mysql
CREATE TRIGGER <triggerName> ON <tableName>
FOR < INSERT | UPDATE | DELETE > AS <SQL-Statement>
```

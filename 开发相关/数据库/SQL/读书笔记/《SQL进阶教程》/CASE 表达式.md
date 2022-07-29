>CASE 表达式是 SQL 里非常重要而且使用起来非常便利的技术，我们应该学会用它来描述条件分支。

## CASE 表达式写法
``` mysql
-- 简单 CASE 表达式 
CASE sex 
	WHEN '1' THEN '男' 
	WHEN '2' THEN '女' 
	ELSE '其他' 
END

-- 搜索 CASE 表达式 
CASE 
	WHEN sex = '1' THEN '男' 
	WHEN sex = '2' THEN '女' 
	ELSE '其他' 
END
```
在发现为真的 WHEN 子句时， CASE 表达式的真假值判断就会中止，而剩余的 WHEN 子句会被忽略。

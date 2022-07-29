>CASE 表达式是 SQL 里非常重要而且使用起来非常便利的技术，我们应该学会用它来描述条件分支。进行不同条件的统计是 CASE 表达式的主要用法之一。
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
```ad-warning
title: 注意
1. 在发现为真的 WHEN 子句时， CASE 表达式的真假值判断就会中止，而剩余的 WHEN 子句会被忽略。
2. 一定要注意 CASE 表 达式里各个分支返回的数据类型是否一致。某个分支返回字符型，而其他 分支返回数值型的写法是不正确的。
3. 不要忘了写 END
4. 与 END 不同，ELSE 子句是可选的，不写也不会出错。不写 ELSE 子句时， CASE 表达式的执行结果是 NULL。
```

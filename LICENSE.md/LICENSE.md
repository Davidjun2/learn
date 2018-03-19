	having与where的区别:
		1.having是在分组后对数据进行过滤.
		  where是在分组前对数据进行过滤
			
	2.having后面可以使用分组函数(统计函数)
		where后面不可以使用分组函数。
		WHERE是对分组前记录的条件，如果某行记录没有满足WHERE子句的条件，那么这行记录不会参加分组；
		而HAVING是对分组后数据的约束。




数据查询语法（DQL）
　　DQL就是数据查询语言，数据库执行DQL语句不会对数据进行改变，而是让数据库发送结果集给客户端。

	语法：
	
	SELECT selection_list 				/*要查询的列名称*/
	FROM table_list 					/*要查询的表名称*/
	WHERE condition 					/*行条件*/
	GROUP BY grouping_columns 			/*对结果分组*/
	HAVING condition 					/*分组后的行条件*/
	ORDER BY sorting_columns			/*对结果分组*/
	LIMIT offset_start, row_count;		/*结果限定*/
	
	example:
	
	SELECT job ,SUM(sal) 
	FROM emp 
	GROUP BY job 
	HAVING SUM(sal)>50000 AND job!='销售员' 
	ORDER BY SUM(sal) ASC ;
	
	
	内连接的特点：查询结果必须满足条件才会显示出来。
	左连接的特点：左连接是先查询出左表（即以左表为主），然后查询右表，右表中满足条件的显示出来，不满足条件的显示NULL。
	右连接的特点：右连接就是先把右表中所有记录都查询出来，然后左表满足条件的显示，不满足显示NULL。
	
	子查询就是嵌套查询，即SELECT中包含SELECT，如果一条语句中存在两个，或两个以上SELECT，那么就是子查询语句了。
		子查询作为条件
		子查询形式为多行单列（当子查询结果集形式为多行单列时可以使用ALL或ANY关键字）















































## autocommit 每个查询当作一个事务;默认采用自动提交

## 1.4 多版本并发控制MVCC 
	各种数据库有不同实现,为减少过多的锁操作
	innodb增加行创建时间,删除时间
	[!img/performance-mysql-mvcc.PNG]
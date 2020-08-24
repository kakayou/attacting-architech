# mysql 日常维护工具

## mysqlcheck
1. mysqlcheck工具中提供了check、repair、analyze、optimize的功能。在执行过程中会对表加锁。
2. mysqlcheck 只能在 mysqld 进程启动的时候使用
3. 只用 MyISAM 存储引擎支持mysqlcheck提供的4中所有操作。

## mysql备份工具
###  mysqlhotcopy vs mysqldump
1. mysqlhotcopy 使用lock tables、flush tables和cp或scp来快速备份数据库.它是备份数据库或单个表最快的途径,完全属亍物理备份,但只能用于备份MyISAM存储引擎和运行在数据库目录所在的机器上.
2. mysqldump属于逻辑备份,备份时是执行的sql语句.

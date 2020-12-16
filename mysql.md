退出mysql终端：
    control+D

mysql设置环境变量：
    PATH="$PATH":/usr/local/mysql/bin;`

启动/关闭数据库服务：
    net start/stop mysql

退出数据库：
    exit

查看有几个数据库/表：
    show databases/tables;

创建/删除数据库：
    create/drop database 数据库名;

使用数据库：
    use 数据库名;

展示表结构：
    desc 表名;in

添加列：
    ALTER TABLE 表名 add column 字段名称 类型(int,char,VARCHAR...) DEFAULT 默认值  位置（FIRST, AFTER+字段名称）;

修改列：
    alter table 表名 modify 列名 varchar(22);

安装/卸载mysql服务
mysqld -remove 
mysqld -install

mysql查看启动参数：
    show variables like 'skip_networking';

初始化mysql：
    mysqld --initialize

执行数据库脚本：
    source 脚本

创建表：
CREATE TABLEmf_fd_cache(
  `id` bigint(18) NOT NULL AUTO_INCREMENT,
  `dep` varchar(3) NOT NULL DEFAULT '',
  `arr` varchar(3) NOT NULL DEFAULT '',
  `flightNo` varchar(10) NOT NULL DEFAULT '',
  `flightDate` date NOT NULL DEFAULT '1000-10-10',
  `flightTime` varchar(20) NOT NULL DEFAULT '',
  `isCodeShare` tinyint(1) NOT NULL DEFAULT '0',
  `tax` int(11) NOT NULL DEFAULT '0',
  `yq` int(11) NOT NULL DEFAULT '0',
  `cabin` char(2) NOT NULL DEFAULT '',
  `ibe_price` int(11) NOT NULL DEFAULT '0',
  `ctrip_price` int(11) NOT NULL DEFAULT '0',
  `official_price` int(11) NOT NULL DEFAULT '0',
  `uptime` datetime NOT NULL DEFAULT '1000-10-10 10:10:10',
  PRIMARY KEY (`id`),
  UNIQUE KEY `uid` (`dep`,`arr`,`flightNo`,`flightDate`,`cabin`),
  KEY `uptime` (`uptime`),
  KEY `flight` (`dep`,`arr`),
  KEY `flightDate` (`flightDate`)
) ENGINE=InnoDB  DEFAULT CHARSET=gbk

创建视图
    CREATE VIEW view_name AS
    SELECT column_name(s)
    FROM table_name
    WHERE condition
#### binlog2kafka
**改写自:[binlog2kafka](https://github.com/runningdata/binlog2kafka)**

在 `GetProperties.java` 文件中修改 canal 和 kafka 的相关配置。

在 `One.java` 文件中可以修改向kafka传送数据的数据格式，当前数据格式为：

```json
{
    "head": {
        "binlog_file": "file_name",
        "binlog_pos": "pos",
        
        "注": "数据库名",
        "db": "database_name", 
        
        "注": "数据表名",
        "table": "table_name",
        
        "注": "取值为INSERT、UPDATE或DELETE",
        "type": "event_type", 
        
        "ctime": "time",
        "exec_time": "time"
    },
    "注": "下面是数据表的各个字段",
    "column1": "value1",
    "column2": "value2",
    "column3": "value3"
}
```


# Paiband - 手环数据库字典文档
- band_admin_log 行为日志表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |             |
|user_id |int(11) |是   |    |   用户名    |
|opt_type |enum(0) |否   |    |   行为类型    |
|mca |varchar(32) |否   |    |   模块_控制器_动作    |
|args |longtext |否   |    |   post数据记录      |
|action_ip     |bigint |是   |    |    执行者ip     |
|remark |longtext     |否   | 0  |   日志备注  |
|created_at |int(11)     |是   | 0  |   注册时间  |
|updated_at |int(11)     |是   | 0  |   修改时间  |


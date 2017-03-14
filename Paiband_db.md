# Paiband - 手环数据库字典文档
-  band_admin_log  行为日志表
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

|字段|类型|空|默认|注释|
|:----    |:-------    |:--- |-- -|------      |
|id      |int(11)     |否   |    |             |
|user_id |int(11) |是   |    |   用户名    |
|opt_type |enum(0) |否   |    |   用户名    |
|mca |varchar(32) |否   |    |   用户名    |
|args |longtext |否   |    |   密码      |
|action_ip     |bigint |是   |    |    昵称     |
|remark |longtext     |否   | 0  |   注册时间  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   注册时间  |
- 备注：无
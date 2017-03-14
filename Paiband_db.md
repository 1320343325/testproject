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

- band_app_versions 应用版本号记录表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|app_version_id      |int(11)     |是   |    |   主键id     |
|build_id |int(11) |是   |    |   版本号ID    |
|versions |varchar |是   |    |   版本号    |
|type |enum |是   |    |   应用包类型：M为固件包，R为软件包    |
|url |varchar |否   |    |   APP下载链接      |
|size     |varchar |否    |    |    APP包大小     |
|isupgrade |int(11)     |是   | 0  |   是否强制升级：0非 1强制  |
|remark     |text |否   |    |    执行者ip     |
|created_at |int(11)     |是   | 0  |   注册时间  |
|updated_at |int(11)     |是   | 0  |   修改时间  |

- band_bind_relation 手环与孩子帐号绑定关系

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |是   |    |   孩子帐号UID     |
|device_id |varchar(64) |是   |    |   设备号    |
|uid |int(11) |是   |    |   家长UID    |
|created_at |int(11)     |是   | 0  |   注册时间  |
|updated_at |int(11)     |是   | 0  |   修改时间  |

- band_child_common 

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |是   |    |   主键id     |
|level |int(11) |是   |    |   等级    |
|total_steps |varchar |是   |    |   总步数    |
|activity_percent80_days |enum |是   |    |   活力指数达到80%的天数    |
|sleep_time_percent90_days |varchar |是   |    |   睡眠时间达到90%的天数      |
|total_motion_time     |varchar |是    |    |    总运动时间     |
|total_stars |int(11)     |是   | 0  |   获得总星星数  |
|total_energy     |text |是   |    |    总获得的能量值     |
|created_at |int(11)     |是   | 0  |   注册时间  |
|updated_at |int(11)     |是   | 0  |   修改时间  |






















































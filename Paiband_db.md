# Paiband - 手环数据库字典文档
- band_admin_log 行为日志表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |             |
|user_id |int(11) |否   |    |   用户名    |
|opt_type |enum(0) |是   |    |   行为类型    |
|mca |varchar(32) |是   |    |   模块_控制器_动作    |
|args |longtext |是   |    |   post数据记录      |
|action_ip     |bigint |否   |    |    执行者ip     |
|remark |longtext     |是   | 0  |   日志备注  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_app_versions 应用版本号记录表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|app_version_id      |int(11)     |否   |    |   主键id     |
|build_id |int(11) |否   |    |   版本号ID    |
|versions |varchar |否   |    |   版本号    |
|type |enum |否   |    |   应用包类型：M为固件包，R为软件包    |
|url |varchar |是   |    |   APP下载链接      |
|size     |varchar |是    |    |    APP包大小     |
|isupgrade |int(11)     |否   | 0  |   是否强制升级：0非 1强制  |
|remark     |text |是   |    |    执行者ip     |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_bind_relation 手环与孩子帐号绑定关系

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |   cid     |
|device_id |varchar(64) |否   |    |   设备号    |
|uid |int(11) |否   |    |   家长UID    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_common 

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |   主键id     |
|level |int(11) |否   |    |   等级    |
|total_steps |int(11) |否   |    |   总步数    |
|activity_percent80_days |enum |否   |    |   活力指数达到80%的天数    |
|sleep_time_percent90_days |int(11) |否   |    |   睡眠时间达到90%的天数      |
|total_motion_time     |int(11) |否    |    |    总运动时间     |
|total_stars |int(11)     |否   | 0  |   获得总星星数  |
|total_energy     |text |否   |    |    总获得的能量值     |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_daily_achievement 每日成就表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|date |int(11) |否   |    |   日期    |
|achievement_id |int(11) |否   |    |   成就任务id    |
|current_value |int(11) |否   |    |   当前完成值    |
|status |tinyint(4) |否   |    |   状态：1：未达成 2：达成未领取 3：达成已领取    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_flowers 小红花

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|current_num |int(11) |否   |    |   当前小红花    |
|reward_num |int(11) |否   |    |   历史奖励小红花数    |
|reward_times |int(11) |否   |    |   奖励次数    |
|exchange_num |int(11) |否   |    |   历史兑换小红花数    |
|exchange_times |int(11) |否   |    |   兑换次数    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_friend 孩子朋友

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|fcid |int(11) |否   |    |   朋友id    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_heart_rate 孩子每天心率数据

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|date |int(11) |否   |    |   日期    |
|light_motion_time |int(11) |否   |    |   轻度运动分钟数    |
|middle_motion_time |int(11) |否   |    |   中度运动分钟数    |
|severe_motion_time |tinyint(4) |否   |    |   重度运动分钟数    |
|lowest_rate |smallint(11) |否   |    |   当天最慢心率    |
|last_real_rate |int(11) |否   |    |   最后的实时心率值    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_long_term_achievement 长期成就表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|achievement_id |int(11) |否   |    |   成就任务id    |
|section |int(11) |否   |    |   阶段    |
|current_value |int(11) |否   |    |   当前值    |
|status |tinyint(4) |否   |    |   状态：1：未达成 2：达成未领取 3：达成已领取    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_motion  孩子每天运动数据

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |   主键id     |
|date |int(11) |否   |    |   日期    |
|steps |int(11) |否   |    |   步数    |
|walk_steps |enum |否   |    |   走的步数  |
|run_steps |int(11) |否   |    |   跑的步数  |
|distance     |int(11) |否    |    |    距离，单位米     |
|calorie |decimal(11)     |否   | 0  |   消耗的卡路里  |
|last_motion_time     |int(11) |否   |    |    最后运动时间     |
|hour_data |text     |否   | 0  |   小时数据，JSON格式  |
|is_complete |tinyint(4)     |否   | 0  |   否否达成目标80%，0：未达成 1：达成  |
|complete_time |int(11)     |否   | 0  |   完成时间  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_settings 孩子设置

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|target_steps |int(11) |否   |    |   步数目标    |
|target_sleep |int(11) |否   |    |   睡眠目标，单位分钟    |
|parent_vision |int(11) |是   |    |   家长愿景，JSON格式    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_child_sleeping 孩子每天睡眠数据

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |   主键id     |
|date |int(11) |否   |    |   日期    |
|fall_asleep_time |int(11) |否   |    |   入睡时间，不包括10到18点的午睡时间    |
|get_up_time |enum |否   |    |   起床时间  |
|sleep_time |int(11) |否   |    |   睡眠时间，单位分钟  |
|deep_sleep_time     |int(11) |否    |    |    深度睡眠时间，单位分钟     |
|light_sleep_time |decimal(11)     |否   | 0  |   晚上浅睡眠时间，单位分钟  |
|noon_sleep_time     |int(11) |否   |    |    午睡睡眠时间，单位分钟     |
|noon_deep_sleep_time |text     |否   | 0  |   午睡深度睡眠时间，单位分钟  |
|noon_light_sleep_time |tinyint(4)     |否   | 0  |   中午浅睡眠时间，单位分钟  |
|awake_count |int(11)     |否   | 0  |   醒来次数  |
|night_awake_count |int(11)     |否   | 0  |   晚上睡觉苏醒次数，不包括10点到18点的午睡时间  |
|daily_sleep_data |int(11)     |否   | 0  |   每日睡眠数据，JSON格式  |
|is_complete |int(11)     |否   | 0  |   是否达成目标的90%,0:未达成 1：达成  |
|complete_time |int(11)     |否   | 0  |   达成时间  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |






































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
|get_up_time |int(11) |否   |    |   起床时间  |
|sleep_time |int(11) |否   |    |   睡眠时间，单位分钟  |
|deep_sleep_time     |int(11) |否    |    |    深度睡眠时间，单位分钟     |
|light_sleep_time |int(11)     |否   | 0  |   晚上浅睡眠时间，单位分钟  |
|noon_sleep_time     |int(11) |否   |    |    午睡睡眠时间，单位分钟     |
|noon_deep_sleep_time |int(11)     |否   | 0  |   午睡深度睡眠时间，单位分钟  |
|noon_light_sleep_time |int(11)    |否   | 0  |   中午浅睡眠时间，单位分钟  |
|awake_count |int(11)     |否   | 0  |   醒来次数  |
|night_awake_count |int(11)     |否   | 0  |   晚上睡觉苏醒次数，不包括10点到18点的午睡时间  |
|daily_sleep_data |int(11)     |否   | 0  |   每日睡眠数据，JSON格式  |
|is_complete |int(11)     |否   | 0  |   是否达成目标的90%,0:未达成 1：达成  |
|complete_time |int(11)     |否   | 0  |   达成时间  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_client 

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |   主键id     |
|name |varchar(100) |否   |    |   游戏名称    |
|game_appid |int(11) |否   |    |   游戏应用ID     |
|data_appid |varchar(64) |否   |    |   纬度成长原始采集数据对应appid  |
|service_id |int(10) |否   |    |   服务号  |
|wd_app_key     |varchar(64) |否    |    |    纬度服务号app_key     |
|wd_secret_key |varchar(64)     |否   | 0  |   纬度服务号secret_key  |
|version_latest     |varchar(50) |否   |    |    最新版本号     |
|lock_time |int(10)     |否   | 0  |   锁屏时间  |
|ver_res_latest |varchar(50)     |否   | 0  |   最新资源号  |
|secret_key |varchar(32)     |否   | 0  |   密钥  |
|server_resource_online |varchar(100)     |否   | 0  |   线上资源域名  |
|server_resource_online_ip |varchar(50)     |否   | 0  |   线上资源IP   |
|server_resource_local_ip |varchar(100)     |否   | 0  |   本地测试  |
|messages |text     |否   | 0  |   APP文案JSON  |
|account_appid |int(11)     |否   | 0  |   帐号接入passport appid  |
|account_secret_key |varchar(64)     |否   | 0  |   孩子帐号接入 passport secret_key  |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_clock 时钟设定

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|clock_id      |int(11)     |否   |    |   id     |
|cid |int(11) |否   |    |   孩子id    |
|cycle |tinyint(4) |否   |    |   周日，1：工作日 2：周末    |
|category |tinyint(4) |是   |    |   类型 1：起床 2：学习 3：运动 4：睡觉 5：其他    |
|repeat |char(8) |是   |    |   是否重复，第8位代表周一，依次类推，第一位预留    |
|time |varchar(8) |是   |    |   时间    |
|is_sync |tinyint(4) |是   |    |   是否同步的状态，1：同步到手环 0：未同步到手环    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_clock_timer_heart_rate 定时心率时钟

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|clock_timer_heart_rate_id      |int(11)     |否   |    |        |
|cid |int(11) |否   |    |   孩子帐号ID    |
|time |varchar(8) |否   |    |   时间    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_common_child_account 孩子帐号游戏关系

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|game_id |int(11) |否   |    |   游戏ID    |
|current_device_id |varchar(128) |否   |    |   当前登录的设备ID，同一设备只记录在最后登录的帐号上    |
|reg_time |int(11) |否   |    |   注册时间    |
|reg_ip |varchar(128) |否   |    |   注册IP    |
|reg_device_id |varchar(128) |否   |    |   注册设备ID    |
|last_login_time |int(11) |否   |    |   最后登录时间    |
|last_login_ip |varchar(128) |否   |    |   最后登录IP    |
|last_login_device_id |varchar(128) |否   |    |   最后登录设备id    |
|last_login_device_name |varchar(64) |否   |    |   最后登录设备名称    |
|play_times |int(11) |否   |    |   游戏次数    |
|game_times |int(11) |否   |    |   游戏时间，分钟数    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_common_child_info 孩子信息表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |        |
|nickname |varchar(64) |否   |    |   孩子昵称    |
|birthday |date |是   |    |   生日    |
|stature |decimal(11) |否   |    |   身高，单位厘米    |
|weight |decimal(11) |否   |    |   体重，单位千克    |
|gender |tinyint(4) |否   |    |   1男 0 女    |
|avatar |varchar(256) |否   |    |   孩子头像    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_common_child_parent 家长孩子关系表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |   孩子帐号ID     |
|uid |int(11) |否   |    |   家长UID    |
|relationship |tinyint(4) |否   |    |   关系，"1" : "父亲","2" : "妈妈","3" : "爷爷","4" : "奶奶","5" : "外公","6" : "外婆","7" : "其他人"    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_common_parent_service 家长关注的服务号

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|game_id      |int(11)     |否   |    |   游戏id     |
|uid |int(11) |否   |    |   家长UID    |
|openid |varchar(64) |否   |    |   家长openid    |
|cid      |int(11)     |否   |    |   通过孩子UID关注的服务号     |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_core_admin_menu 菜单

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|menu_name |varchar(32) |是   |    |   菜单组名    |
|status |tinyint(1) |是   |    |   状态    |
|sort      |smallint(3)     |是   |    |   排序     |
|icon |varchar(32) |是   |    |   图标    |
|created_at |timestamp     |是   | 0  |   注册时间  |
|updated_at |timestamp     |是   | 0  |   修改时间  |

- band_core_admin_permission 权限

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|permission_name |varchar(16) |是   |    |   权限名称    |
|mca |varchar(32) |是   |    |   模块_控制器_动作    |
|menu_id      |int(11)     |是   |    |   模块id     |
|is_nav |tinyint(1) |是   |    |   是否加入导航    |
|status |tinyint(1) |是   |    |   1,正常 2，禁用 默认1    |
|icon |varchar(32) |是   |    |   图标    |
|created_at |timestamp     |是   | 0  |   注册时间  |
|updated_at |timestamp     |是   | 0  |   修改时间  |

- band_core_admin_role 角色

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|role_name |varchar(64) |是   |    |   角色名称    |
|status |tinyint(1) |是   |    |   角色状态 1, 正常 2,禁用    |
|created_at |timestamp     |是   | 0  |   注册时间  |
|updated_at |timestamp     |是   | 0  |   修改时间  |

- band_core_admin_role_permission 角色

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|role_id      |int(11)     |是   |    |        |
|permission_id |int(11)  |是   |    |   权限id    |
|menu_id |int(11)  |是   |    |   模块id    |
|status |tinyint(1) |是   |    |   状态 1 正常 2 禁用    |
|created_at |timestamp     |是   | 0  |   注册时间  |
|updated_at |timestamp     |是   | 0  |   修改时间  |

- band_core_admin_user 后台管理员

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|email |varchar(64)  |是   |    |   用户邮箱    |
|password |varchar(32)  |是   |    |   用户密码    |
|salt |varchar(8)  |是   |    |       |
|status |tinyint(1) |是   |    |   用户状态,1:正常，0：禁用    |
|realname |varchar(15) |是   |    |   用户姓名    |
|super_admin |tinyint(1) |是   |    |   1，非管理 2，管理员    |
|created_at |timestamp     |是   | 0  |   注册时间  |
|updated_at |timestamp     |是   | 0  |   修改时间  |

- band_core_admin_user_role 管理员对应的角色

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|user_id      |int(11)     |否   |    |        |
|role_id |int(11)  |否   |    |   角色id    |
|status |tinyint(1)  |否   |    |   角色状态 1,正常 2,禁用    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_core_cron 执行

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cron_id      |int(11)     |否   |    |        |
|command |varchar(1024)  |否   |    |   命令    |
|schedule |varchar(128)  |否   |    |   执行配置，同linux crontab   |
|exec_count |int(11)  |否   |    |   总执行次数    |
|last_exec_time |int(11)  |否   |    |   最后执行时间    |
|status |tinyint(4)  |否   |    |   状态，1：发布 2：未发布 3：过期    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_core_cron_log 执行日志

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|cron_id |int(11)  |否   |    |   命令    |
|result |smallint(4)  |否   |    |   执行结果，1：成功 2：失败   |
|msg |text  |否   |    |   消息，包括错误信息等    |
|start_time |decimal(20)  |否   |    |   开始时间    |
|end_time |decimal(20)  |否   |    |   结束时间    |
|exec_time |decimal(20)  |否   |    |   最后执行时间    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_filter_ip 

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|ip |int(11)  |是   |    |   ip    |
|status |tinyint(1)  |是   |    |   状态    |

- band_food 食物能量表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|category |tinyint(4)  |否   |    |   食物类别：1:脂肪 2:垃圾食品 3:蛋白 4:钙 5:锌 6:铁 7:维生素A 8:维生素B 9:维生素C 10:维生素D 11:纤维素    |
|name |varchar(32)  |否   |    |   名称    |
|content |varchar(32)  |否   |    |   内容    |
|calorie |int(11)  |否   |    |   每100g热量（kcal）    |
|icon |varchar(256)  |否   |    |   图标    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_food_calorie 食物热量配置

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |        |
|food_name |tinyint(4)  |否   |    |   食物名称    |
|food_unit |varchar(32)  |否   |    |   单位    |
|kcal |varchar(32)  |否   |    |   热量    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_help 帮助中心

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|help_id      |int(11)     |否   |    |        |
|title |varchar(150)  |否   |    |   名称    |
|url |varchar(255)  |否   |    |   文章链接地址    |
|content |text  |否   |    |   内容    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_light_screens 抬腕亮屏设定

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |    孩子CID    |
|open_time |varchar(8)  |否   |    |   开启时间    |
|close_time |varchar(8)  |否   |    |   关闭时间    |
|status |tinyint(2)  |否   |    |   状态：0关闭 1开启，默认开启    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_light_screens 抬腕亮屏设定

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|cid      |int(11)     |否   |    |    孩子CID    |
|open_time |varchar(8)  |否   |    |   开启时间    |
|close_time |varchar(8)  |否   |    |   关闭时间    |
|status |tinyint(2)  |否   |    |   状态：0关闭 1开启，默认开启    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_child_flowers 小红花LOG

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|log_child_flowers_id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|type |tinyint(2)  |否   |    |   类型：1奖励 2兑换    |
|num |int(11)  |否   |    |   数量：奖励或兑换小红花数量    |
|old_num |int(11)  |否   |    |   之前小红花    |
|remark |varchar(255)  |否   |    |   备注    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_heart_rate 心率日志

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|device_id |varchar(64)  |否   |    |   设备id    |
|rate |int(11)  |否   |    |   心率值    |
|collect_time |bigint(20)  |否   |    |   心率采集时间点    |
|status |tinyint(4)  |否   |    |   心率状态：1：走路 2：跑步    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_motion 运动日志

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|device_id |varchar(64)  |否   |    |   设备id    |
|steps |int(11)  |否   |    |   当前累积步数    |
|motion_time |bigint(20)  |否   |    |   当前状态的开始时间    |
|status |tinyint(4)  |否   |    |   运动状态：0：静止 1：走路 2：跑步    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_motion_energy 运动获得的能量值log

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|log_motion_energy_id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|num |varchar(64)  |否   |    |   获得的能量数    |
|steps |int(11)  |否   |    |   运动总步数    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_push_weidu 推送和返回数据记录

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|band_log_push_weidu_id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|open_id |text  |否   |    |   json格式的open_id    |
|service_id |int(10)  |否   |    |   service_id    |
|content_data |text  |是   |    |   发送的数据    |
|template_id |varchar(255)  |否   |    |   模板id    |
|url |varchar(255)  |是   |    |   跳转的链接地址    |
|back_content |text  |是   |    |   返回的数据    |
|created_at |int(11)     |是   | 0  |   注册时间  |
|updated_at |int(11)     |是   | 0  |   修改时间  |

- band_log_sleeping 睡眠日志

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|device_id |varchar(64)  |否   |    |   设备号    |
|time |bigint(20)  |否   |    |   状态的时间    |
|status |int(11)  |否   |    |   状态 0：深睡 1：浅睡 2：醒着    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_sleeping_energy 睡眠获得的能量值log

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|log_sleeping_energy_id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|num |int(11)  |否   |    |   获得的能量数    |
|quality |tinyint(2)  |否   |    |   睡眠质量：4为很差    |
|sleep_time |int(11)  |否   |    |   总睡眠时间，单位分钟    |
|deep_sleep_time |int(11)  |否   |    |   深度睡眠时间，单位分钟    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_log_sleeping_energy 睡眠获得的能量值log

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|log_timer_heart_rate_id      |int(11)     |否   |    |    自增ID    |
|cid |int(11)  |否   |    |   孩子CID    |
|device_id |varchar(64)  |否   |    |   设备ID    |
|rate |int(2)  |否   |    |   心率值    |
|collect_time |bigint(11)  |否   |    |   心率采集时间点    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_sports 运动

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |    自增ID    |
|category |tinyint(4)  |否   |    |   1:家务 2:运动锻炼 3:球类 4:灵敏协调    |
|weather |varchar(32)  |是   |    |   天气要素    |
|times |varchar(32)  |是   |    |   时段要素    |
|age |varchar(32)  |是   |    |   年龄段    |
|stature |varchar(32)  |是   |    |   身高评价    |
|bmi |varchar(32)  |是   |    |   BMI评价    |
|name |varchar(32)  |否   |    |   名称    |
|calorie |decimal(11)  |否   |    |   消耗热量,消耗热量数值单位（大卡/每公斤/分）    |
|example |varchar(128)  |否   |    |   视频事例    |
|icon |varchar(256)  |否   |    |   图标    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_strategy_motion 推荐方案-运动

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(1)     |否   |    |    自增ID    |
|age |varchar(32)  |是   |    |   年龄段    |
|stature |varchar(32)  |是   |    |   身高评价    |
|bmi |varchar(32)  |是   |    |   BMI评价    |
|content |text  |是   |    |   内容    |
|icon |varchar(256)  |是   |    |   图标    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_strategy_pabulum 推荐方案-营养

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(1)     |否   |    |    自增ID    |
|age |varchar(32)  |是   |    |   年龄段    |
|stature |varchar(32)  |是   |    |   身高评价    |
|bmi |varchar(32)  |是   |    |   BMI评价    |
|content |text  |是   |    |   内容    |
|icon |varchar(256)  |是   |    |   图标    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_sys_config 系统配置表

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|sys_config_id      |int(1)     |否   |    |    自增ID    |
|name |varchar(255)  |是   |    |   参数名：大写英文    |
|sys_value |text  |是   |    |   配置对应的值    |
|remark |varchar(255)  |是   |    |   备注    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_tips_common 通用小贴士

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(1)     |否   |    |    自增ID    |
|category |tinyint(4)  |否   |    |   1：运动 2：睡眠 3：心率 4:营养    |
|content |varchar(1024)  |否   |    |   内容    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_tips_season 季节天气提示

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(1)     |否   |    |    自增ID    |
|season |tinyint(4)  |否   |    |   季节：1：春 2：夏 3：秋 4：冬    |
|content |varchar(1024)  |否   |    |   内容    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |

- band_tips_target 目标提示

| 字段          | 类型           | 空  | 默认  | 注释  |
| ------------- |:-------------:| -----:|-----:|-----:|
|id      |int(11)     |否   |    |    自增ID    |
|category |tinyint(4)  |否   |    |   类别 1：运动 2：睡眠 3：心率    |
|cycle |tinyint(4)  |否   |    |   周期，1：日 2：周 3：月    |
|complete |tinyint(4)  |否   |    |   完成度，1：100及以上 2：80~99 3：60~79  4：60以下    |
|content |varchar(1024)  |否   |    |   内容    |
|created_at |int(11)     |否   | 0  |   注册时间  |
|updated_at |int(11)     |否   | 0  |   修改时间  |





























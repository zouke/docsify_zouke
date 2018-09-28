 
# changren
### api\_doc
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| doc_content| text| 接口公共文档内容| |YES|
| create_time| datetime| 添加时间| |YES|
| update_time| datetime| 修改时间| |YES|
| doc_title| varchar| | |YES|
### api\_ip\_ask\_log
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| ip| varchar| 访问接口的客户端ip地址| |NO|
| ask_url| varchar| 访问接口的完整url| |NO|
| create_time| datetime| 访问时间| |NO|
| token| varchar| Http请求header中的token值| |NO|
| ask_from| varchar| 接口访问来源（app、机器人）| |NO|
### api\_ip\_ask\_num
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| ip| varchar| | |YES|
| num| tinyint| 接口暴力调用的次数| 3|YES|
### cr\_check\_device -- 检测设备
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| check_device_name| varchar| 检测检测名称| |YES|
| create_time| datetime| 创建时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_check\_device\_item -- 设备检测项
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| check_device_id| int| 设备检测对应的id| 10|YES|
| check_item_id| int| 检测项id| 10|YES|
| create_time| datetime| 创建时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_check\_item -- 设备检测项
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| check_item_name| varchar| 检测项,对应表名(blood_pressure、blood_sugar、blood_oxygen、cholesterol、electrocardio、purine_trione、temprature)| |YES|
| create_time| datetime| 创建时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_family -- 家庭组信息
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| fname| varchar| 家庭组名称| |NO|
| create_user_id| int| 家庭组创建者用户ID| 10|NO|
| create_time| datetime| 创建时间| |NO|
| type| tinyint| 类型(1-家庭、2-药店)| 3|YES|
### cr\_index\_blood\_\_blood\_oxygen -- 血氧检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| spo2| decimal| 血氧饱和度,单位:%| 1|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_blood\_oxygen -- 血氧检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| spo2| decimal| 血氧饱和度,单位:%| 1|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_blood\_pressure -- 血压检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| diastolic_blood_pressure| smallint| 收缩压(SYS),单位:mmHg| 5|NO|
| systolic_blood_pressure| smallint| 舒张压(DIA),单位:mmHg| 5|NO|
| pulse_rate| smallint| 心率,单位:bpm| 5|NO|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_blood\_sugar -- 血糖检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| empty_stomach| decimal| 空腹血糖含量,单位:mmol/l| 1|YES|
| after_meal| decimal| 饭后血糖含量,单位:mmol/l| 1|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_bmi -- BMI检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| bmi| decimal| 体质指数| 2|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_electrocardio -- 心电检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| etc| text| 心率值--波形图,单位:bpm,格式(json):[{"datetime":"2018-01-01 00:00:00","value":"20"},{"datetime":"2018-01-01 00:00:01","value":"30"},{"datetime":"2018-01-01 00:00:02","value":"40"}]| |YES|
| hrv| tinyint| 心率变异性| 3|YES|
| heart_rate| tinyint| 心率，单位:次/分| 3|YES|
| respiratory_rate| tinyint| 呼吸率| 3|NO|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测指标对应的id| 10|NO|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_report -- 健康检测参数分析汇总
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| url| varchar| 报告地址| |YES|
| generate_time| datetime| 报告生成时间| |YES|
### cr\_index\_sleep -- 睡眠检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| hour| tinyint| 睡眠时间| 3|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测对应的id| 10|YES|
| check_time| datetime| 检测时间| |NO|
### cr\_index\_temprature -- 体温检测参数
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| temp| tinyint| 体温,单位:℃| 3|YES|
| index| tinyint| 健康指数(评分)| 3|NO|
| tip| text| 健康提示建议| |YES|
| check_device_item_id| int| 设备检测对应的id| 10|YES|
| check_time| datetime| 检测时间| |NO|
### cr\_people\_ill\_history -- 病史信息列表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| ill_history_name| varchar| 病史名称| |NO|
| create_time| datetime| 添加时间| |NO|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_people\_taboos -- 禁忌药品信息列表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| taboos_name| varchar| 禁忌药品名称| |NO|
| create_time| datetime| 添加时间| |NO|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_plan\_blood\_sugar -- 血糖健康计划
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| power| int| 能量，单位:kcal| 10|NO|
| food| int| 食物类,单位:g| 10|NO|
| create_time| datetime| 创建时间| |NO|
### cr\_robot\_device -- 机器人设备
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| sn| varchar| 设备唯一识别码| |YES|
| sn_type| tinyint| 设备类型| 3|YES|
| type| tinyint| 机器人所属类型(1-家庭、2-药店)| 3|NO|
### cr\_robot\_family\_rel -- 机器人-家庭关系表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| robot_device_id| varchar| 机器人设备id| |NO|
| family_id| int| 家庭id| 10|NO|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
| create_time| datetime| 创建时间| |NO|
### cr\_user -- 用户个人信息表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| tel| varchar| 手机号| |YES|
| password| varchar| 密码| |YES|
| email| varchar| 邮箱| |YES|
| user_name| varchar| 用户姓名| |YES|
| nick_name| varchar| 昵称| |YES|
| idcard| varchar| 身份证号| |YES|
| sex| tinyint| 性别,1男、2女| 3|YES|
| avatar| varchar| 用户头像存放地址| |YES|
| birth| date| 生日| |YES|
| weight| smallint| 体重,单位:kg| 5|YES|
| stature| smallint| 身高,单位:cm| 5|YES|
| tabboos_ids| varchar| 用户禁忌药品id,格式:1,2,3,4,5| |YES|
| allergens_ids| varchar| 过敏原id,格式:1,2,3,4,5| |YES|
| ill_history_ids| varchar| 病史id,格式:1,2,3,4,5| |YES|
| status| tinyint| 注册状态(1.待填写基本信息 2.待提交健康信息 3.待创建家庭 4.已注册)| 3|NO|
| is_delete| tinyint| 是否删除,1是、0.否| 3|NO|
| update_time| datetime| 更新时间| |YES|
| create_time| datetime| 注册时间| |NO|
### cr\_user\_allergens -- 过敏原信息
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| allergens_name| varchar| 过敏原名称| |YES|
| create_time| datetime| 添加时间| |YES|
| update_time| datetime| 修改时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_user\_family\_rel -- 用户-家庭关系表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| user_id| int| 用户id| 10|NO|
| family_id| int| 家庭id| 10|NO|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
| create_time| datetime| 创建时间| |NO|
### cr\_user\_ill\_history -- 病史信息
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| ill_history_name| varchar| 病史名称| |YES|
| create_time| datetime| 添加时间| |YES|
| update_time| datetime| 修改时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### cr\_user\_taboos -- 禁忌药品信息
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| taboos_name| varchar| 禁忌药品名称| |YES|
| create_time| datetime| 添加时间| |YES|
| update_time| datetime| 修改时间| |YES|
| is_deleted| tinyint| 是否删除,1是、0否| 3|NO|
### system\_auth -- 系统权限表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 20|NO|
| title| varchar| 权限名称| |NO|
| status| tinyint| 状态(1:禁用,2:启用)| 3|YES|
| sort| smallint| 排序权重| 5|YES|
| desc| varchar| 备注说明| |YES|
| create_by| bigint| 创建人| 20|YES|
| create_at| timestamp| 创建时间| |YES|
### system\_auth\_node -- 系统角色与节点绑定
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 20|NO|
| auth| bigint| 角色ID| 20|YES|
| node| varchar| 节点路径| |YES|
### system\_config -- 系统参数配置
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| name| varchar| 配置编码| |YES|
| value| varchar| 配置值| |YES|
### system\_log -- 系统操作日志表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 20|NO|
| ip| char| 操作者IP地址| |NO|
| node| char| 当前操作节点| |NO|
| username| varchar| 操作人用户名| |NO|
| action| varchar| 操作行为| |NO|
| content| text| 操作内容描述| |NO|
| create_at| timestamp| 创建时间| |NO|
### system\_menu -- 系统菜单表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 20|NO|
| pid| bigint| 父id| 20|NO|
| title| varchar| 名称| |NO|
| node| varchar| 节点代码| |NO|
| icon| varchar| 菜单图标| |NO|
| url| varchar| 链接| |NO|
| params| varchar| 链接参数| |YES|
| target| varchar| 链接打开方式| |NO|
| sort| int| 菜单排序| 10|YES|
| status| tinyint| 状态(0:禁用,1:启用)| 3|NO|
| create_by| bigint| 创建人| 20|NO|
| create_at| timestamp| 创建时间| |YES|
### system\_node -- 系统节点表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| int| | 10|NO|
| node| varchar| 节点代码| |YES|
| title| varchar| 节点标题| |YES|
| is_menu| tinyint| 是否可设置为菜单| 3|YES|
| is_auth| tinyint| 是否启动RBAC权限控制| 3|YES|
| is_login| tinyint| 是否启动登录控制| 3|YES|
| create_at| timestamp| 创建时间| |YES|
### system\_sequence -- 系统序号表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 19|NO|
| type| varchar| 序号类型| |YES|
| sequence| char| 序号值| |NO|
| create_at| timestamp| | |YES|
### system\_user -- 系统用户表
 
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |
|--------| --------| --------|--------|--------|
| id| bigint| | 20|NO|
| username| varchar| 用户登录名| |NO|
| password| char| 用户登录密码| |NO|
| qq| varchar| 联系QQ| |YES|
| mail| varchar| 联系邮箱| |YES|
| phone| varchar| 联系手机号| |YES|
| desc| varchar| 备注说明| |YES|
| login_num| bigint| 登录次数| 20|YES|
| login_at| datetime| | |YES|
| status| tinyint| 状态(0:禁用,1:启用)| 3|NO|
| authorize| varchar| | |YES|
| is_deleted| tinyint| 删除状态(1:删除,0:未删)| 3|YES|
| create_by| bigint| 创建人| 20|YES|
| create_at| timestamp| 创建时间| |YES|

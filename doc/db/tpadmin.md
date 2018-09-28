   
# tpadmin  
### tp\_admin\_access  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| node_id| smallint| | 5|NO  
| level| tinyint| | 3|NO  
| pid| smallint| | 5|NO  
### tp\_admin\_group  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| | |NO  
| icon| varchar| icon小图标| |NO  
| sort| int| | 10|NO  
| status| tinyint| | 3|NO  
| remark| varchar| | |NO  
| isdelete| tinyint| | 3|NO  
| create_time| int| | 10|NO  
| update_time| int| | 10|NO  
### tp\_admin\_node  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| pid| smallint| | 5|NO  
| group_id| tinyint| | 3|NO  
| name| varchar| | |NO  
| title| varchar| | |NO  
| remark| varchar| | |NO  
| level| tinyint| | 3|NO  
| type| tinyint| 节点类型，1-控制器 | 0-方法| 3|NO  
| sort| smallint| | 5|NO  
| status| tinyint| | 3|NO  
| isdelete| tinyint| | 3|NO  
### tp\_admin\_node\_load -- 节点快速导入  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| title| varchar| 标题| |NO  
| name| varchar| 名称| |NO  
| status| tinyint| 状态| 3|NO  
### tp\_admin\_role  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| pid| smallint| 父级id| 5|NO  
| name| varchar| 名称| |NO  
| remark| varchar| 备注| |NO  
| status| tinyint| 状态| 3|NO  
| isdelete| tinyint| | 3|NO  
| create_time| int| | 10|NO  
| update_time| int| | 10|NO  
### tp\_admin\_role\_user  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| user_id| char| | |YES  
### tp\_admin\_user  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| account| char| | |NO  
| realname| varchar| | |NO  
| password| char| | |NO  
| last_login_time| int| | 10|NO  
| last_login_ip| char| | |NO  
| login_count| mediumint| | 7|NO  
| email| varchar| | |NO  
| mobile| char| | |NO  
| remark| varchar| | |NO  
| status| tinyint| | 3|NO  
| isdelete| tinyint| | 3|NO  
| create_time| int| | 10|NO  
| update_time| int| | 10|NO  
### tp\_app\_channel -- app渠道表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| app_name| varchar| app名字| |NO  
| app_version| varchar| app版本号| |YES  
| app_code| varchar| app标识（2：安卓。3：ios）| |YES  
| channel_code| varchar| 渠道标识| |YES  
| channel_name| varchar| 渠道名字| |NO  
| create_time| datetime| 创建时间| |NO  
| sort| int| 排序值| 10|NO  
### tp\_app\_log -- 操作日志  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| message_before| text| 操作前记录| |YES  
| message_after| text| 操作后记录| |YES  
| create_user| varchar| 操作人| |YES  
| create_time| datetime| 操作时间| |YES  
| type| int| 1添加、2修改、3删除| 10|YES  
| message| varchar| | |YES  
### tp\_app\_msg -- 发送App消息
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"1(商品详情页)","itemid":"商品sku\_id","sno":"商品sku\_no","activity\_type":"活动商品才有","activity\_id":"活动商品id(活动商品专有)"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"2(关联模块)","plate\_type":"1限时蜂抢、2新品、3蜂神榜、4蜂觅、5首页"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"3(消息富文本)","rich\_text\_id":"消息富文本id"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"4(H5页面)","url":"H5页面地址"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"5(蜂雷头条详情页)","id":"蜂雷头条id"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"6(订单详情)","order\_no":"订单号"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"7(我的零库存页)","id":"productType的id(跳转0库存要用)","buyerId":"用户id(跳转0库存要用)","inventoryType":"0库存标识"}  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| icon| varchar| 消息图标地址| |YES  
| title| varchar| 消息标题| |YES  
| subject| varchar| 消息简介| |YES  
| ad_link_type| int| 跳转方式(1商品详情页、2关联模块、3消息富文本、4H5页面、5蜂雷头条详情页、6订单详情、7我的库存)| 10|YES  
| ad_link_content| text| 广告链接内容 (json格式)| |YES  
| send_time| datetime| 发送时间| |YES  
| send_method| tinyint| 发送方式(1实时发送、2定时发送)| 3|YES  
| send_status| tinyint| 发送状态   1已发送  2未发送| 3|NO  
| create_id| bigint|  创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| update_id| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|NO  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|NO  
### tp\_app\_open\_ad -- 开屏广告
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"1(商品详情页)","itemid":"商品sku\_id","sno":"商品sku\_no"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"2(关联模块)","plate\_type":"1限时蜂抢、2新品、3蜂神榜、4蜂觅、5首页"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"3(消息富文本)","rich\_text\_id":"消息富文本id"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"4(H5页面)","url":"H5页面地址"}
{"ad\_type":"一级分类(默认1)","ad\_link\_type":"5(蜂雷头条详情页)","id":"蜂雷头条id"}  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| second| int| 开屏广告停留时长(单位:秒)| 10|YES  
| ad_effective_start| datetime| 开屏广告有效时间--开始时间| |YES  
| ad_effective_end| datetime| 开屏广告有效时间--结束时间| |YES  
| ad_url| varchar|  开屏广告图片地址| |YES  
| ad_link_type| int| 广告链接类型(1商品详情页、2关联模块、3消息富文本、4H5页面、5蜂雷头条详情页)| 10|YES  
| ad_link_content| text| 广告链接内容 (json格式)| |YES  
| create_id| bigint|  创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| update_id| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|NO  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|NO  
### tp\_app\_tracelog -- app追踪表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| username| varchar| 用户名| |YES  
| app_code| varchar| app标识（2：安卓。3：ios）| |YES  
| app_version| varchar| app版本号| |YES  
| init_time| datetime| app启动时间| |NO  
| channel_code| varchar| 渠道标识| |YES  
| create_time| datetime| 创建时间| |YES  
| devices| text| 用户设备信息| |NO  
### tp\_app\_version -- app版本  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| type| char| app类型：ios,android| |NO  
| version| int| 版本号| 10|NO  
| version_name| varchar| 版本名称| |YES  
| must_update| tinyint| 是否强制更新（1：是）| 3|NO  
| filename| varchar| 文件名称| |YES  
| img| varchar| 更新背景图片| |YES  
| url| varchar| | |YES  
| up_content| text| 更新内容| |YES  
| created| datetime| 创建时间| |YES  
| modified| datetime| 修改时间| |YES  
| create_id| bigint| 创建人id| 19|YES  
| update_id| bigint| 修改人id| 19|YES  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|NO  
| status| tinyint| 状态： 1 正常 2 禁用| 3|NO  
### tp\_avatar\_head\_pic -- 默认头像表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| style_id| varchar| 风格id| |NO  
| type_id| int| 类型id| 10|YES  
| theme_id| int| 主题id| 10|YES  
| img| varchar| 图片| |YES  
| sort| int| 排序| 10|YES  
| create_time| datetime| 创建时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| update_id| bigint| 修改人| 19|YES  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|NO  
| status| tinyint| 状态： 1 正常 2 禁用| 3|NO  
### tp\_avatar\_style -- 风格表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 风格名称| |YES  
| create_time| datetime| 创建时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| update_id| bigint| 修改人| 19|YES  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|YES  
### tp\_avatar\_theme -- 默认图片主题表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 主题名称| |NO  
| update_id| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|YES  
### tp\_avatar\_type -- 默认图片类型表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 类别名称| |NO  
| update_id| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|YES  
### tp\_decorate\_shop\_template -- 用户店铺装修表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 模板标题| |YES  
| plate_content| text| 内容配置项（json格式）| |YES  
| status| smallint| 状态： 1已开启、2已暂停| 5|YES  
| create_time| datetime| 创建时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| update_id| bigint| 最后修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| img| varchar| 样式图| |YES  
| goods_nums| varchar| 可选商品数量| |NO  
| is_default| int| 是否默认(1是、2否)| 10|NO  
| is_deleted| int| 是否删除(0否、-1删除)| 10|NO  
### tp\_decorate\_user\_shop -- 店铺装修模板表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| plate_id| varchar| 模板样式id| |YES  
| plate_content_draft| text| 蜂店装修草稿模板内容| |YES  
| plate_content| text| 蜂店装修显示的模板| |YES  
| status| tinyint| 模板状态： 1草稿、2发布| 3|YES  
| create_time| datetime| 创建时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| update_id| bigint| 最后修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| use_status| tinyint| 使用状态(1-未使用、2已使用)| 3|NO  
| select_status| tinyint| 选中状态(1否、2是）| 3|NO  
### tp\_doc\_log\_info -- 开发日志信息--log记录  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| version_id| int| 版本id| 10|YES  
| interface_name| varchar| 接口名称| |YES  
| doc_posion| varchar| 文档位置| |YES  
| type| int| 更新类型(1新增、2修改)| 10|YES  
| desc| varchar| 备注| |YES  
| desc_detail| text| 详细备注| |YES  
| subject_id| int| 项目id| 10|YES  
| create_time| int| 添加时间| 10|YES  
| update_time| int| 修改时间| 10|YES  
| status| tinyint| 禁用状态| 3|NO  
| isdelete| tinyint| 删除状态| 3|NO  
| sort| smallint| 排序| 5|NO  
### tp\_doc\_return\_info -- 接口返回实例  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| interface_name| varchar| 接口名称| |YES  
| return| text| 返回实例--JSON| |YES  
| subject_id| int| 项目id| 10|YES  
| create_time| int| 添加时间| 10|YES  
| update_time| int| 修改时间| 10|YES  
| status| tinyint| 禁用状态| 3|NO  
| isdelete| tinyint| 删除状态| 3|NO  
| sort| smallint| 排序| 5|NO  
### tp\_doc\_subject -- 项目名称  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| subject| varchar| 项目名称(app、h5、manage、inner_open)| |YES  
| create_time| int| 添加时间| 10|YES  
| update_time| int| 修改时间| 10|YES  
| status| tinyint| 禁用状态| 3|NO  
| isdelete| tinyint| 删除状态| 3|NO  
| sort| smallint| 排序| 5|NO  
### tp\_doc\_subject\_config  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| module| varchar| 模块名| |YES  
| dir| varchar| 接口注释所在目录| |YES  
| title| varchar| 接口文档标题栏| |YES  
| domain| varchar| 接口访问域名| |YES  
| create_time| int| 添加时间| 10|YES  
| update_time| int| 修改时间| 10|YES  
| status| tinyint| 禁用状态| 3|NO  
| isdelete| tinyint| 删除状态| 3|NO  
| sort| smallint| 排序| 5|NO  
### tp\_doc\_version -- 开发日志版本--log记录  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| version| varchar| 版本号| |YES  
| create_time| int| 创建时间| 10|YES  
| update_time| int| 修改时间| 10|YES  
| status| tinyint| 禁用状态| 3|NO  
| isdelete| tinyint| 删除状态| 3|NO  
| sort| smallint| 排序| 5|NO  
### tp\_express -- 快递表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| kdname| varchar| 快递全称| |NO  
| express_s| varchar| 快递缩写| |NO  
| expname| varchar| 英文缩写| |NO  
| idorder| smallint| 排序| 5|NO  
| yn| tinyint| 是否锁定  1正常 0锁定| 3|NO  
| waybill_type| tinyint| 0普通面单1电子面单| 3|YES  
| taobao_code| varchar| 淘宝编码| |YES  
| express_template| text| 打印模板| |NO  
| status| tinyint| 状态：0:不显示；1：显示| 3|YES  
| regex| varchar| 正规表达式| |NO  
| modified| datetime| 同步时间| |YES  
### tp\_file  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| cate| tinyint| 文件类型，1-image | 2-file| 3|NO  
| name| varchar| 文件名| |NO  
| original| varchar| 原文件名| |NO  
| domain| varchar| | |NO  
| type| varchar| | |NO  
| size| int| | 10|NO  
| mtime| int| | 10|NO  
### tp\_gift\_goods\_sku -- sku商品赠品表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| parent_sku_no| varchar| 关联赠品的商品编号| |YES  
| sku_no| varchar| 赠品sku编号| |YES  
| num| int| 赠品数量| 10|YES  
| create_time| datetime| 创建时间| |YES  
| is_deleted| tinyint| 是否删除（0：正常，-1:删除）| 3|NO  
| is_online| tinyint| 状态可选值：1（上架）、0（下架）| 3|YES  
| modified| datetime| 更新时间| |YES  
| update_user| bigint| 修改人| 19|YES  
| create_user| bigint| 创建人| 19|YES  
| type| int| 赠品赠送类型:1-按商品数倍增、2-固定值| 10|NO  
### tp\_gift\_goods\_sku\_stock -- 赠品库存表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| sku_no| varchar| 赠品sku编号| |YES  
| stock| int| 赠品库存数量| 10|YES  
| create_time| datetime| 创建时间| |YES  
| is_deleted| tinyint| 是否删除（0：正常，-1:删除）| 3|NO  
| is_online| tinyint| 状态可选值：1（上架）、0（下架）| 3|YES  
| modified| datetime| 更新时间| |YES  
| update_user| bigint| 修改人| 19|YES  
| create_user| bigint| 创建人| 19|YES  
### tp\_gift\_log -- 商品增品操作日志表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| message| text| 日志记录内容| |YES  
| create_time| datetime| 创建时间| |YES  
| create_id| bigint| 创建人| 19|YES  
| type| int| 日志类型:1赠品库存管理、2商品赠品管理| 10|YES  
| sku_no| varchar| 商品或赠品编号| |YES  
### tp\_gift\_order\_goods -- 订单商品赠品表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| parent_sku_no| varchar| order_goods sku编号| |YES  
| sku_no| varchar| 赠品sku编号| |YES  
| num| int| 赠品数量| 10|YES  
| create_time| datetime| 创建时间| |YES  
| order_no| varchar| 订单号| |YES  
| stock_num| int| 赠品库存量| 10|YES  
| package_id| char| 包裹号| |YES  
### tp\_goods -- 商品表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| product_id| varchar| 对外的商品ID,字段唯一索引| |YES  
| goodstype_id| smallint| 商品类型| 5|NO  
| propsclass_id| varchar| 规格类型ID| |NO  
| brand_id| smallint| 商品品牌| 5|NO  
| sale_protection| text| 售后描述| |YES  
| content| text| 商品描述| |YES  
| unit_id| smallint| 商品单位| 5|NO  
| title| varchar| 商品标题| |NO  
| supplier_id| varchar| 供应商| |NO  
| created| datetime| 创建时间| |NO  
| modified| datetime| 修改时间| |NO  
| cost_price| decimal| 成本价| 10|YES  
| sync_time| datetime| 同步时间| |YES  
| seascapes| text| 海景图片组 字符串| |YES  
| search_name| varchar| 商品搜索名称| |YES  
| is_deleted| tinyint| 是否删除（0：正常，-1:删除）| 3|NO  
| is_online| tinyint| 状态可选值：1（上架）、0（下架）| 3|YES  
| img| varchar| | |YES  
| imgs| text| 商品图片组| |YES  
| status| varchar| | |YES  
| merchant| varchar| 供应商标识| |YES  
| merchant_type| tinyint| 供应商类型，1：供应商，2：销售商，3：供销一体| 3|YES  
### tp\_goods\_attr -- 商品规格分类表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 属性名| |NO  
| status| varchar| 状态。可选值:normal(正常),deleted(删除)| |NO  
| modified| datetime| 修改时间| |YES  
| sort_order| int| 排列序号。取值范围:大于零的整数| 10|NO  
| distant_sign| int| 远端标识(远程对应规格id)| 10|NO  
| merchant| varchar| 供应商标识| |YES  
### tp\_goods\_brand -- 品牌表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| brand_name| varchar| 品牌名称| |NO  
| logo_path| varchar| 品牌logo| |YES  
| brand_keywords| varchar| 品牌别名| |NO  
| brand_url| varchar| 品牌网址| |NO  
| status| varchar| 状态。可选值:normal(正常),deleted(删除)| |YES  
| modified| datetime| 修改时间| |YES  
| margin_money| decimal| 保证金| 11|NO  
| margin_status| tinyint| 是否缴纳保证金： 1 否 2 是| 3|YES  
| distant_sign| int| 远端标识| 10|NO  
| distant_come_time| datetime| 远端同步时间| |YES  
### tp\_goods\_sku -- 商品sku表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| product_id| varchar| 对应goods表中的product_id| |NO  
| prom_id| int| 促销id| 10|NO  
| sku_id| varchar| 数字编号| |NO  
| sku_no| varchar| sku编号| |YES  
| barcode| varchar| 条码| |NO  
| title| varchar| 商品标题| |NO  
| short_name| varchar| 只用于提示用语| |NO  
| properties| varchar| 规格| |NO  
| unit_id| smallint| 单位ID| 5|NO  
| average_price| decimal| 动态采购价| 11|NO  
| sell_price| decimal| 零售价| 10|YES  
| cost_price| decimal| 成本价就是采购价| 11|NO  
| market_price| decimal| 市场价| 10|YES  
| retail_price| float| 零售价| 11|NO  
| supplier_id| varchar| 供货商ID| |NO  
| weight| int| 重量| 10|NO  
| yuding| tinyint| 是否可预定| 3|NO  
| pic_path| varchar| 产品图片地址| |YES  
| inventory| tinyint| 盘点| 3|NO  
| tag_no| varchar| 库位编号| |NO  
| nd_pt_bar| tinyint| 是否需要入库时打印条形码| 3|NO  
| nd_ck_bar| tinyint| 核对条形码OFF/ON| 3|NO  
| nd_ck_weight| tinyint| 核定重量| 3|NO  
| has_commission| tinyint| 是否提成SKU 1代表TRUE,0代表FALSE| 3|NO  
| status| tinyint| 状态(0 下架 1 上架 )| 3|NO  
| gift| tinyint| 是否可以作为赠品，0是不可以1是可以| 3|YES  
| is_invoice| tinyint| 是否带发票 0 否 1是| 3|YES  
| sync_time| datetime| 同步时间| |YES  
| soft_text| varchar| 软文组：多个以逗号隔开| |YES  
| restriction| varchar| 限购数量(0：不限购)| |YES  
| img| varchar| 图片| |YES  
| feelee_commission| varchar|  蜂享规则(包含用户类型，返佣值，返佣类型）| |YES  
| deductible_currency| decimal| 抵扣蜂雷币| 11|YES  
| sell_nums| int| 销售数量| 10|NO  
| hits| int| 点击数| 10|NO  
| warning_line| int| 预警线| 10|YES  
| recommend_index| int| 推荐指数| 10|YES  
| comment_num| int| 评论数量| 10|NO  
| content| varchar| | |YES  
| is_zero_goods| tinyint| 是否为0元购(1：0元购。0：不是0元购)| 3|NO  
| is_flcoin_deduction| tinyint| '是否峰雷币抵扣（0：不抵扣，1：抵扣| 3|YES  
| is_deleted| tinyint| 是否删除（0：正常，-1:删除）| 3|NO  
| update_time| datetime| 更新时间| |YES  
| virtual_inventory| int| 虚拟库存| 10|NO  
| feelee_mark| tinyint| 1：蜂享商品| 3|NO  
| goods_type| tinyint| 商品所属类型 1：平台商品   2特色商品| 3|NO  
| update_user| bigint| 修改人| 19|YES  
| create_user| bigint| 创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| publish_time| datetime| 发布时间（上架时间）| |YES  
| is_open_bee| tinyint| 是否开启蜂仓   1已开启   2未开启| 3|NO  
| deductible_cash| decimal| 抵扣现金| 11|NO  
| is_show| tinyint| 是否展示（0：展示，1：不展示）| 3|NO  
| inventory_min_price| decimal| 库存最低价| 11|YES  
| is_group| tinyint| 是否为组合SKU(0:否,1:是)| 3|YES  
| wholesale_virtual_inventory| int| 批发的虚拟库存| 10|YES  
| wholesale_sales_nums| int| 批发销量| 10|YES  
| merchant| varchar| 供应商标识| |YES  
| merchant_type| tinyint| 供应商类型，1：供应商，2：销售商，3：供销一体| 3|YES  
| have_gift| tinyint| 是否设置为有赠品（1：有赠品）| 3|NO  
### tp\_goods\_sku\_sell\_recording -- 用户购买库限购记录表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| goods_itemid| varchar| 商品编号或者是sku_id| |NO  
| type| tinyint| 类型：1：sku,2:goods| 3|NO  
| num| int| 购买数量| 10|YES  
| user_id| bigint| 用户编号| 19|NO  
| activity_id| int| 活动id| 10|YES  
| activity_type| int| 活动类型（1:限时蜂抢）| 10|YES  
| create_time| datetime| 创建时间| |NO  
### tp\_goods\_unit -- 商品单位表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 单位名| |NO  
| reid| smallint| | 5|NO  
| status| varchar| 状态。可选值:normal(正常),deleted(删除)| |YES  
| modified| datetime| 修改时间| |YES  
| distant_sign| int| 远端标识(远程单位id)| 10|NO  
### tp\_invoice\_template -- 发票模板  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| company_name| varchar| 企业名称| |YES  
| taxpayer_no| varchar| 纳税人识别号| |YES  
| register_mobile| varchar| 注册电话| |YES  
| register_address| varchar| 注册地址| |YES  
| account_bank| varchar| 开户行| |YES  
| account_bank_no| varchar| 银行账户| |YES  
| is_default| tinyint| 是否默认 1 默认 2 非默认| 3|YES  
| status| tinyint| 状态(1草稿2待审核4已驳回8已通过)| 3|YES  
| remark| varchar| 备注（驳回原因）| |YES  
| create_user| varchar| 创建者| |YES  
| create_time| datetime| 创建时间| |YES  
| update_time| datetime| 更新时间| |YES  
| type| tinyint| 发票类型:1-普票、2-增票| 3|NO  
| is_deleted| tinyint| 是否删除(-1是、0否)| 3|NO  
### tp\_login\_log  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| uid| mediumint| | 7|NO  
| login_ip| char| | |NO  
| login_location| varchar| | |NO  
| login_browser| varchar| | |NO  
| login_os| varchar| | |NO  
| login_time| timestamp| | |NO  
### tp\_node\_map -- 节点图  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| module| varchar| 模块| |NO  
| controller| varchar| 控制器| |NO  
| action| varchar| 方法| |NO  
| method| char| 请求方式| |NO  
| comment| varchar| 节点图描述| |NO  
### tp\_one\_two\_three\_four -- 四级控制器  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| field1| varchar| 字段一| |YES  
| option| varchar| 选填| |YES  
| select| varchar| 下拉框| |YES  
| radio| varchar| 单选| |YES  
| checkbox| varchar| 复选框| |YES  
| password| varchar| 密码| |YES  
| textarea| varchar| 文本域| |YES  
| date| varchar| 日期| |YES  
| mobile| varchar| 手机号| |YES  
| email| varchar| 邮箱| |YES  
| sort| smallint| 排序| 5|YES  
| status| tinyint| 状态，1-正常 | 0-禁用| 3|NO  
| isdelete| tinyint| 删除状态，1-删除 | 0-正常| 3|NO  
| create_time| int| 创建时间| 10|NO  
| update_time| int| 更新时间| 10|NO  
### tp\_promotion -- 活动表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| type| char| 促销类型(1-限时抢购、2-商品活动专场)| |YES  
| title| varchar| 标题| |YES  
| img| varchar| 图片| |YES  
| status| char| 状态(1-正常、2-删除)| |YES  
| audit_status| char| 审核状态(1-审核通过、2-审核不通过)| |YES  
| audit_time| datetime| 审核时间| |YES  
| start_time| datetime| 开始时间| |YES  
| end_time| datetime| 结束时间| |YES  
| create_user| varchar| | |YES  
| create_time| datetime| | |YES  
| update_user| varchar| | |YES  
| update_time| datetime| | |YES  
### tp\_promotion\_goods -- 活动商品表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| product_id| varchar| 对外的商品ID,字段唯一索引| |YES  
| promotion_id| int| 促销编码| 10|YES  
| title| varchar| 商品标题| |YES  
| sell_price| decimal| 销售价格| 11|YES  
| total_inventory| int| 总库存| 10|YES  
| search_name| varchar| 商品搜索名称| |YES  
| img| varchar| | |YES  
| status| char| 状态(1-正常、2-删除)| |YES  
| state| char| 上下架(1-上架、2-下架)| |YES  
| create_user| varchar| | |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| | |YES  
| update_time| datetime| 修改时间| |YES  
### tp\_promotion\_goods\_sku -- 活动商品sku表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| product_id| varchar| 对应goods表中的product_id| |YES  
| promotion_id| int| 促销id| 10|YES  
| title| varchar| 商品标题| |YES  
| search_name| varchar| 商品搜索名称| |YES  
| sku_id| varchar| 数字编号| |YES  
| sku_no| varchar| | |YES  
| status| char| 状态(1正常、2-删除)| |YES  
| state| char| 上下架(1-上架、2-下架)| |YES  
| current_inventory| int| 当前库存| 10|YES  
| promotional_price| decimal| 促销价格| 11|YES  
| cost_price| decimal| 成本价| 11|NO  
| restriction| int| 用户限购数量| 10|YES  
| sales_number| int| 销售数量| 10|YES  
| img| text| 图片| |YES  
| selling_time| datetime| 销售时间| |YES  
| create_user| varchar| | |YES  
| create_time| datetime| | |YES  
| update_user| varchar| | |YES  
| update_time| datetime| 更新时间| |YES  
### tp\_quotao\_authority\_goods  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| authority_quota_id| int| 授权订单额度表id| 10|YES  
| order_no| varchar| 订单号| |YES  
| sku_id| varchar| 商品属性ID| |YES  
| authority_price| decimal| 授权商品价格| 10|YES  
| create_time| datetime| 创建时间| |YES  
| create_id| int| 创建人| 10|YES  
| update_time| datetime| 修改时间| |YES  
| update_id| int| 修改人| 10|YES  
### tp\_quotao\_authority\_order -- 优惠授权  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| order_no| varchar| 订单号| |YES  
| authority_price| decimal| 授权价格| 10|YES  
| reason| varchar| 申请理由| |YES  
| real_payment| decimal| 实付款| 10|YES  
| create_time| datetime| 创建时间| |YES  
| create_id| int| 创建人id| 10|YES  
| update_time| datetime| 修改时间| |YES  
| update_id| int| 修改人id| 10|YES  
| authority_status| tinyint| 授权状态(1已授权、2拒绝授权、3审核中)| 3|NO  
| authority_refuse_reason| varchar| 授权拒绝理由| |YES  
| imgs| text| 优惠凭证图片列表| |YES  
### tp\_quotao\_employee -- 员工额度  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| personnel_code| int| 员工编号| 10|YES  
| use_start_time| datetime| 使用开始时间| |YES  
| use_end_time| datetime| 使用结束时间| |YES  
| use_quota| decimal| 已使用额度| 10|YES  
| total_quota| decimal| 总额度| 10|YES  
| is_deleted| tinyint| 是否删除，0未删除、-1已删除| 3|NO  
| status| tinyint| 员工状态（1正常、2禁用）| 3|NO  
| create_time| datetime| 创建时间| |YES  
| create_id| int| 创建人ID| 10|YES  
| update_time| datetime| 修改时间| |YES  
| update_id| int| 修改人id| 10|YES  
### tp\_quotao\_log -- 员工优惠授权操作日志表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| message| varchar| 操作日志| |YES  
| create_id| bigint| 操作人| 19|YES  
| create_time| datetime| 操作时间| |YES  
| type| tinyint| 日志类型:1-订单列表、2-额度管理| 3|NO  
| order_no| varchar| 订单号| |YES  
| personnel_code| int| 员工编号| 10|YES  
### tp\_red\_envelopes -- 红包表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| user_id| varchar| 红包发送人| |YES  
| type| char| 1、普通红包2、拼手气红包| |YES  
| red_envelopes_no| varchar| 红包编码| |YES  
| red_envelopes_count| int| 红包数量| 10|YES  
| red_envelopes_total| decimal| 红包总金额| 11|YES  
| single_money| decimal| 单个金额| 11|YES  
| send_status| char| 1、未发送2、已经发送| |YES  
| send_time| datetime| 发送时间| |YES  
| source| char| 来源(0、安卓 1、ios 2、H5 3、pc4、php)| |YES  
| pay_type| char| 支付方式支付方式(1-支付宝、2-零钱、3-微信、4-大额支付)| |YES  
| pay_status| char| 付款状态(1-未付款、2-付款)| |YES  
| pay_time| datetime| 支付时间| |YES  
| final_pay| decimal| 实付金额| 11|YES  
| content| varchar| 内容| |YES  
| available_count| int| 可用数量| 10|YES  
| available_money| decimal| 可用金额| 12|YES  
| confirm_settlement| char| 是否确认结算1、未结算2、已结算| |YES  
| version| int| 版本号| 10|YES  
| pull_red_code| varchar| 拉新红包编码| |YES  
| create_user| varchar| 创建人| |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| 修改人| |YES  
| update_time| datetime| 修改时间| |YES  
| is_recharge_pay| char| 是否充值支付(0-否、1是)| |YES  
### tp\_red\_envelopes\_code  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| user_id| varchar| 手机号| |YES  
| ip| varchar| ip| |YES  
| check_code| varchar| 验证码| |YES  
| img_check_code| varchar| 图片验证码| |YES  
| effective_time| int| 验证码有效时间（分钟）| 10|YES  
| type| char| 1.注册 2.其他| |YES  
| status| char| 状态 1.已验证 2.未验证 3.无效验证码 4.其他| |YES  
| source| char| 来源(0-安卓、1-ios、2-H5、3-pc、4-php)| |YES  
| create_user| varchar| 创建人| |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| 修改人| |YES  
| update_time| datetime| 修改时间| |YES  
### tp\_red\_envelopes\_detail -- 红包详情表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| user_id| varchar| 红包领取人| |YES  
| status| char| 1-正常状态、2-锁定状态、3-领取状态| |YES  
| code| varchar| | |YES  
| user_token| varchar| 唯一标识| |YES  
| red_envelopes_no| varchar| 红包编码| |YES  
| envelopes_money| decimal| 红包金额| 11|YES  
| create_user| varchar| 创建人| |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| 修改人| |YES  
| update_time| datetime| 修改时间| |YES  
### tp\_red\_envelopes\_log -- 红包日志表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| red_envelopes_no| varchar| 红包编码| |YES  
| node_name| varchar| 日志订单节点说明| |YES  
| status| char| 操作状态| |YES  
| create_user| varchar| 操作人| |YES  
| create_time| datetime| 操作时间| |YES  
| remark| varchar| 备注| |YES  
### tp\_red\_envelopes\_pay -- 红包支付信息表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| red_envelopes_no| varchar| 红包编码| |YES  
| pay_account_name| varchar| 付款帐号名称| |YES  
| pay_account_no| varchar| 付款帐号| |YES  
| order_money| decimal| 订单总金额| 12|YES  
| pay_status| char| 付款状态(1-未付款、2-付款)| |YES  
| pay_trade_no| varchar| 支付流水号| |YES  
| out_trade_no| varchar| 第三方交易流水号| |YES  
| pay_type| char| 支付方式(1-支付宝、2-零钱、3-其他支付)| |YES  
| pay_time| datetime| 付款时间| |YES  
| pay_money| decimal| 付款金额| 12|YES  
| remark| varchar| 备注| |YES  
| create_user| varchar| 创建人| |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| 修改人| |YES  
| update_time| datetime| 修改时间| |YES  
### tp\_red\_envelopes\_pay\_log -- 红包支付日志表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| red_envelopes_no| varchar| 红包编码| |YES  
| type| char| 1-支付、2-回调| |YES  
| pay_type| char| 支付方式(1-支付宝、2-零钱、3-其他支付)| |YES  
| pay_trade_no| varchar| 支付流水号| |YES  
| out_trade_no| varchar| 第三方交易流水号| |YES  
| request_params| text| 请求参数| |YES  
| response_params| text| 返回参数| |YES  
| remark| varchar| 备注| |YES  
| create_user| varchar| 创建人| |YES  
| create_time| datetime| 创建时间| |YES  
| update_user| varchar| 修改人| |YES  
| update_time| datetime| 修改时间| |YES  
### tp\_store\_category\_ad -- 分类广告  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| cate_id| int| 分类id| 10|YES  
| ad_url| varchar| 分类广告图片地址| |YES  
| ad_link_type| int| 广告链接类型(1商品详情页、2关联模块、3商品列表、4H5页面、5蜂雷头条详情页、6订单详情、7零钱明细、8蜂雷币明细、9订单列表)| 10|YES  
| ad_link_content| text| 广告链接内容 (json格式)| |YES  
| create_id| bigint|  创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| update_id| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| status| tinyint| 状态： 1 正常 2 禁用| 3|NO  
| is_deleted| tinyint| 是否已删除 0正常  1 已删除| 3|NO  
### tp\_store\_goods -- 店铺商品关联表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| store_id| bigint| 店铺id| 19|YES  
| sku_id| varchar| 商品属性id| |YES  
| sku_no| varchar| 商品属性编号| |YES  
| product_id| varchar| 商品id| |YES  
| g_cats| text| 商品所属分类path| |YES  
| update_user| bigint| 修改人| 19|YES  
| update_time| datetime| 修改时间| |YES  
| create_user| bigint| 创建人| 19|YES  
| create_time| datetime| 创建时间| |YES  
| pt_cats| text| 平台所属分类path| |YES  
| is_deleted| tinyint| 是否已删除 1 正常  0 已删除| 3|NO  
| is_open| tinyint| 是否显示 0否 1是| 3|NO  
| merchant| varchar| 供应商标识| |YES  
### tp\_store\_goods\_category -- 店铺商品分类表  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| name| varchar| 分类名称| |NO  
| store_id| bigint| 对应店铺表id(第一级时指定store_id)| 19|YES  
| path| text| 层级路径（以/分隔）| |YES  
| type_id| bigint| 分类类型（1平台商品，2特色商品）| 19|YES  
| img| varchar| 分类图片| |YES  
| sort| int| 排序| 10|YES  
| is_deleted| tinyint| 是否已删除 1 正常  0 已删除| 3|NO  
| is_open| tinyint| 是否显示 0否 1是| 3|YES  
| update_user| bigint| | 19|YES  
| update_time| datetime| | |YES  
| create_user| bigint| | 19|YES  
| create_time| datetime| | |YES  
| merchant| varchar| 供应商标识| |YES  
### tp\_web\_log\_001 -- 网站日志  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| uid| smallint| 用户id| 5|NO  
| ip| char| 访客ip| |NO  
| location| varchar| 访客地址| |NO  
| os| varchar| 操作系统| |NO  
| browser| varchar| 浏览器| |NO  
| url| varchar| url| |NO  
| module| varchar| 模块| |NO  
| controller| varchar| 控制器| |NO  
| action| varchar| 方法| |NO  
| method| char| 请求方式| |NO  
| data| text| 请求的param数据，serialize后的| |YES  
| create_at| int| 操作时间| 10|NO  
### tp\_web\_log\_all -- 网站日志  
   
| 字段名 | 字段类型 | 字段注释 | 字段存储长度 | 是否为空 |  
|--------| --------| --------|--------|--------|  
| uid| smallint| 用户id| 5|NO  
| ip| char| 访客ip| |NO  
| location| varchar| 访客地址| |NO  
| os| varchar| 操作系统| |NO  
| browser| varchar| 浏览器| |NO  
| url| varchar| url| |NO  
| module| varchar| 模块| |NO  
| controller| varchar| 控制器| |NO  
| action| varchar| 方法| |NO  
| method| char| 请求方式| |NO  
| data| text| 请求的param数据，serialize后的| |YES  
| create_at| int| 操作时间| 10|NO  

## 1. getGoodsListByCate --- 邹柯

### 1.1 功能描述

根据分类获取商品列表

### 1.2 请求说明

> 请求方式：POST

> 请求URL：Category/getGoodsListByCate? 调用参数说明:body--POST--格式:{"method":"Category.getGoodsListByCate","source":"1","type":"other","store_id":"","type_in":"1","sort":"1","keywords":"117082948985098","cate_type":"","brand_id":"","page":"1","pagesize":"10"}

### 1.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| type | 是 | string | 店铺类型--首页进去(other)、我的蜂店进去(me)|
| type_in | 是 | int | 搜索入口--1首页、2分类页、3店铺装修分类|
| store_id | 否 | string | 店铺id|
| source | 是 | int | 来源(1--h5、2--app)|
| sort | 否 | int | 排序字段(1销量由高到低、2价格由低到高、3价格由高到低)--不传默认1|
| keywords | 否 | string | 搜索字段(商品名称、店铺id、店铺名称)|
| cate_type | 否 | string | 商品所属分类--格式:13,20,24,16|
| brand_id | 否 | string | 品牌id--格式:3,4,5,6|
| page | 否 | int | 页码(不传默认1)|
| pagesize | 否 | int | 每页显示条数(不传默认10)|
### 1.4 返回结果

```json

{
	"data":{
		"information":[{
			"avatar":"http://blog.minhow.com",
			"nickname":"minhow",
			"age":"25"
		}],
		"news":[{
			"title":"minhow",
			"content":"I am MinHow"
		}]
	},
	"code":"200",
	"msg":"SUCCESS"
}

```

### 1.5 返回参数

| 字段 | 字段说明 |
|--------| --------|
| 【1】分类入口搜索返回字段说明 | |
| select_status | 选中状态(1是、2否)|
| img | 宫格图片|
| seascapes | 海景图|
| sell_nums | 已卖数量|
| sku_id | 商品属性id|
| sku_no | 商品属性编号|
| title | 商品标题|
| sell_price | 零售价|
| store_id | 店铺id|
| is_zero_goods | 是否为0元购(1|
| restriction | 限购数量|
| yuding | 是否可预定|
| market_price | 市场价|
| cost_price | 成本价|
| profit | 利润|
| spec_name | 规格名称|
| activity_info---|    |
| activityId | 活动编码|
| activityType | 活动类型|
| productPrice | 活动售价|
| costPrice | 成本价|
| title | 活动标题|
| isAct | 是否是活动(true|
| >>>foot | |
| current_page | 当前页|
| pagesize | 每页显示条数|
| total_page | 总页数|
| >>>cate_info | |
| id | 分类id|
| name | 分类名称|
| list_status | 1选中、2未选中|
| >>>brand_info | |
| id | 品牌id|
| brand_name | 品牌名称|
| list_status | 1选中、2未选中|
| 【2】首页入口搜索返回字段说明 | |
| >>>store_goods-------|    |
| focus | 关注状态(1已关注、2未关注)|
| head_sculpture | 头像|
| is_self | 店铺标识(other其他店铺、me登录用户店铺)|
| name | 店铺名称|
| personal_sign | 个性签名|
| store_id | 店铺id|
| username | 用户昵称|
| version | 店铺版本|
| goods | |
| ----img | 商品图片|
| sell_price | 零售价|
| sku_id | 商品sku_id|
| sku_no | 商品sku编码|
| store_id | 店铺id|
| >>>goods_goods-------|    |
| img | 图片|
| sell_nums | 已卖数量|
| sku_id | 商品属性id|
| sku_no | 商品属性编号|
| title | 商品标题|
| sell_price | 零售价|
| store_id | 店铺id|
| is_zero_goods | 是否为0元购(1|
| restriction | 限购数量|
| yuding | 是否可预定|
| market_price | 市场价|
| cost_price | 成本价|
| profit | 利润|
| spec_name | 规格名称|
| activity_info---|    |
| activityId | 活动编码|
| activityType | 活动类型|
| productPrice | 活动售价|
| costPrice | 成本价|
| title | 活动标题|
| isAct | 是否是活动(true|
| >>>foot | |
| current_page | 当前页|
| pagesize | 每页显示条数|
| total_page | 总页数|
| >>>cate_info | |
| id | 分类id|
| name | 分类名称|
| list_status | 1选中、2未选中|
| >>>brand_info | |
| id | 品牌id|
| brand_name | 品牌名称|
| list_status | 1选中、2未选中|
| >>>recommend_goods-------|    |
| >>>goods_info | 参数说明同上|
| activity_info---|    |
| activityId | 活动编码|
| activityType | 活动类型|
| productPrice | 活动售价|
| costPrice | 成本价|
| title | 活动标题|
| isAct | 是否是活动(true|
| >>>list_type-------1显示推荐商品、2不显示推荐商品|    |
| total_count | 总商品数或总店铺数(不包括精确搜索的店铺数)|
-----------------------

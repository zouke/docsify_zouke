## 1. GoodsManageList --- andy

### 1.1 功能描述

 商品综合管理列表

### 1.2 请求说明

> 请求方式：POST

> 请求URL：GoodsManage/GoodsManageList? 调用参数:{"skuId":"8032717999","username":"13248258731","method":"GoodsManage.GoodsManageList","check_code":"123456"}  此接口要登录

### 1.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| actId | 否 | string | 活动id|
| skuId | 是 | string | 商品sku_id|
| username | 是 | string | 用户账户|
### 1.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"\u6210\u529f",
	"result":{
		"specs":[{
			"spec_name":"\u957f\u5ea6:1.8\u7c73 ",
			"sku_id":"8032716369",
			"sku_no":"P007528-01",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:25\u7c73 ",
			"sku_id":"8032716370",
			"sku_no":"P007528-09",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:20\u7c73 ",
			"sku_id":"8032716371",
			"sku_no":"P007528-08",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:15\u7c73 ",
			"sku_id":"8032716372",
			"sku_no":"P007528-07",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:12\u7c73 ",
			"sku_id":"8032716373",
			"sku_no":"P007528-06",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:10\u7c73 ",
			"sku_id":"8032716374",
			"sku_no":"P007528-05",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:8\u7c73 ",
			"sku_id":"8032716375",
			"sku_no":"P007528-04",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:5\u7c73 ",
			"sku_id":"8032716376",
			"sku_no":"P007528-03",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:3\u7c73 ",
			"sku_id":"8032716377",
			"sku_no":"P007528-02",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:30\u7c73 ",
			"sku_id":"8032716378",
			"sku_no":"P007528-11",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:1.5\u7c73 ",
			"sku_id":"8032716379",
			"sku_no":"P007528-10",
			"product_id":"P007528"
		},
		{
			"spec_name":"\u957f\u5ea6:6\u7c73 ",
			"sku_id":"8032716380",
			"sku_no":"P007528-12",
			"product_id":"P007528"
		}],
		"userInfo":{
			"username":"13248258731",
			"nick":"13248258731"
		},
		"skuType":false,
		"profit":{
			"sellPrice":null,
			"costPrice":"156.75",
			"profit":"-156.75"
		},
		"sellStatistics":{
			"sellCount":0,
			"sellAmount":"0.00",
			"sellCostPrice":"0.00",
			"arrivedProfit":"0.00"
		},
		"honeycomb":{
			"type":false,
			"avgPrice":null,
			"stock":null,
			"isOpenService":true,
			"isOpenBee":"2",
			"isExistence":"0"
		}
	}
}

```

### 1.5 返回参数

   无
-----------------------

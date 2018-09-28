## 1. getShopDecorateStyle --- 邹柯

### 1.1 功能描述

蜂店样式列表

### 1.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/getShopDecorateStyle? 调试参数:{"method":"FlagShipShopDecorate.getShopDecorateStyle","type_id":"1"}

### 1.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| type_id | 是 | int | 装修商品的类型(1-平台商品、2-特色商品)|
### 1.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"\u6210\u529f",
	"result":[{
		"id":"1",
		"goods_nums":"50",
		"name":"\u9ed8\u8ba4\u6837\u5f0f",
		"preview":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/user\/20180614\/62bed15289674582554.png",
		"list_status":2
	}]
}

```

### 1.5 返回参数

   无
-----------------------
## 2. decorateShop --- 邹柯

### 2.1 功能描述

装修店铺

### 2.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/decorateShop? 调试参数:{"operate_type":"1","username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.decorateShop","plate_id":1,"type":8,"sort":"3","sku_id": "8032717999","index":"1","type_id":"1"}

### 2.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| plate_id | 是 | int | 店铺装修样式ID|
| type | 是 | int | 模板样式子板块类型(4-海景、6-二宫格、8-三宫格、9-四宫格)|
| sort | 是 | int | 模块排序位置|
| sku_id | 是 | string | 商品sku_id|
| index | 是 | int | 商品sku排序位置|
| operate_type | 是 | int | 1-替换商品、2-删除商品|
| type_id | 否 | int | 装修商品的类型(1-平台商品、2-特色商品)|
### 2.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":true
}

```

### 2.5 返回参数

   无
-----------------------
## 3. fabu --- 邹柯

### 3.1 功能描述

发布

### 3.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/fabu? 调试参数:{"username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.fabu"}

### 3.3 请求参数

   无
### 3.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"该样式已发布成功",
	"result":[]
}

```

### 3.5 返回参数

   无
-----------------------
## 4. selectShopDecorate --- 邹柯

### 4.1 功能描述

选中蜂店装修模板样式

### 4.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/selectShopDecorate? 调试参数:{"username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.selectShopDecorate","plate_id":"71","type_id":"1"}

### 4.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| plate_id | 是 | int | 商品(平台或特色)装修样式ID|
| type_id | 是 | int | 要装修商品的类型(1-平台、2-特色)|
### 4.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":[]
}

```

### 4.5 返回参数

   无
-----------------------
## 5. getShopDecorateStyleOne --- 邹柯

### 5.1 功能描述

获取发布的蜂店模板样式

### 5.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/getShopDecorateStyleOne? 调试参数:{"username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.getShopDecorateStyleOne","type":"1","store_id":"115066910197999","type_id":"1"}

### 5.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| store_id | 是 | string | 店铺id|
| type | 是 | int | 装修模板的状态:1-预览蜂店装修模板样式、2-正式发布的蜂店装修模板样式|
| type_id | 否 | int | 要装修商品的类型(1-平台、2-特色)|
### 5.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":{
		"plate_id":"46",
		"list":[{
			"type":4,
			"isShow":"2",
			"sort":1,
			"goods":[{
				"sku_id":"1002975101",
				"operate_type":2,
				"index":1,
				"type":4,
				"product_num":"1",
				"search_name":"无线路由器wifi穿墙 信号放大 覆盖范围广",
				"short_name":"斐讯K2",
				"sku_no":"P001219-01",
				"title":"斐讯（PHICOMM）K2 1200M智能双频无线路由器 ",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I0\/5aa8d44648d05.jpg",
				"sell_price":"399.00",
				"activity_info":{
					"productId":"P001219",
					"skuNo":"P001219-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"66825",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I9\/P001219\/P001219-xyqsNNNDrC.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I5\/P002975\/P002975-65BSz8DPmY.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I5\/P002975\/P002975-409oFe6y5R.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I9\/P001219\/P001219-JsN1EpDf5p.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I9\/5a1e81afa85f2.jpg"]
			}]
		},
		{
			"type":4,
			"isShow":"1",
			"sort":2,
			"goods":[{
				"sku_id":"8012614169",
				"operate_type":2,
				"index":2,
				"type":4,
				"product_num":"1",
				"search_name":"预售 2018年3月31日前统一发货 全渠道首批发货",
				"short_name":"NAS",
				"sku_no":"P002026-01",
				"title":"【预售】斐讯（PHICOMM）天天链N1 新一代家庭专业NAS云盘 珍珠白",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I3\/5a6af2a558fc5.jpg",
				"sell_price":"1499.00",
				"activity_info":{
					"productId":"P002026",
					"skuNo":"P002026-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"10983",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I0\/5a6af1d051e53.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I2\/5a6af1d2349ff.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a6af1d496d26.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I7\/5a6af1d7ccae3.jpg"]
			}]
		},
		{
			"type":4,
			"isShow":"1",
			"sort":3,
			"goods":[{
				"sku_id":"8041111858",
				"operate_type":2,
				"index":3,
				"type":4,
				"product_num":"1",
				"search_name":"1TB存储容量 轻薄机身 type-c接口 USB3.0协议 高速传输",
				"short_name":"斐讯H1",
				"sku_no":"P002330-01",
				"title":"斐讯（PHICOMM） H1 移动硬盘 ",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/goods\/20180411\/a68db15234153762907.jpg",
				"sell_price":"999.00",
				"activity_info":{
					"productId":"P002330",
					"skuNo":"P002330-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"6942",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/server\/goods\/20180428\/d0e8c15248997668431.png",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/server\/goods\/20180411\/5459d15234153678189.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/server\/goods\/20180411\/02b5c15234153694863.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/server\/goods\/20180411\/b86ce15234153713606.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/server\/goods\/20180411\/86d0815234153734114.jpg"]
			}]
		},
		{
			"type":8,
			"isShow":"1",
			"sort":4,
			"goods":[{
				"sku_id":"8012911722",
				"operate_type":2,
				"index":4,
				"type":8,
				"product_num":"",
				"search_name":"深入清洁牙齿缝隙和牙线 有效缓解牙齿敏感",
				"short_name":"多效防敏小苏打牙膏",
				"sku_no":"P002023-01",
				"title":"艾禾美 多效防敏小苏打牙膏 127g",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I1\/5a6e8b4d0d69d.jpg",
				"sell_price":"10.00",
				"activity_info":{
					"productId":"P002023",
					"skuNo":"P002023-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"4243",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a6e8b3cb5a1e.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I2\/5a6e8b3a55b85.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I0\/5a6e8b42498da.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I2\/5a6e8b4415a01.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a6e8b4606e52.jpg"]
			},
			{
				"sku_id":"1227883301",
				"operate_type":2,
				"index":5,
				"type":8,
				"product_num":"",
				"search_name":" CADR值=350立方米每小时 节能静音",
				"short_name":"PHICOMM\/斐讯 悟净A1空气净化器",
				"sku_no":"P001788-01",
				"title":"斐讯（PHICOMM） 悟净A1空气净化器 智能操控 除甲醛PM2.5有害气体 ",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I5\/5a4447016c6bd.jpg",
				"sell_price":"1999.00",
				"activity_info":{
					"productId":"P001788",
					"skuNo":"P001788-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"3611",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I5\/5a44466b3470f.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I0\/5a444670dc152.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a4446748a00c.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I8\/5a4446789d516.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I2\/5a44467c4b1c4.jpg"]
			},
			{
				"sku_id":"8022517282",
				"operate_type":2,
				"index":6,
				"type":8,
				"product_num":"",
				"search_name":"双星定位 IP67防水防尘 心率监测 睡眠监测",
				"short_name":"斐讯智能运动手环 W1",
				"sku_no":"P002080-01",
				"title":"斐讯（PHICOMM）智能运动手环 W1",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I2\/5a935cc6726b8.jpg",
				"sell_price":"799.00",
				"activity_info":{
					"productId":"P002080",
					"skuNo":"P002080-01",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"3219",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I6\/5a92689290fa7.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I9\/5a9268951f274.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I1\/5a9268971ff81.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a92689a83e2d.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I6\/5a92689cd3547.jpg"]
			}]
		},
		{
			"type":4,
			"isShow":"1",
			"sort":5,
			"goods":[{
				"sku_id":"8031411009",
				"operate_type":2,
				"index":7,
				"type":4,
				"product_num":"1",
				"search_name":"哈曼国际联合打造 高智能语音交互 智能家居 语音助手",
				"short_name":"AI智能音箱",
				"sku_no":"P002086-02",
				"title":"斐讯（PHICOMM）AI智能音箱语音机器人 R1",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I1\/5aaba37587497.jpg",
				"sell_price":"2499.00",
				"activity_info":{
					"productId":"P002086",
					"skuNo":"P002086-02",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"2880",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I1\/5aaba36149de9.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I8\/5aaba35eaa034.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I1\/5aaba2d5dc537.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I8\/5aaba2dce430a.jpg",
				"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I9\/5aaba2dd303a5.jpg"]
			}]
		},
		{
			"type":9,
			"isShow":"1",
			"sort":6,
			"goods":[{
				"sku_id":"1000000003",
				"operate_type":2,
				"index":8,
				"type":9,
				"product_num":"",
				"search_name":"店铺标准版",
				"short_name":"标准版",
				"sku_no":"FL001001-04",
				"title":"蜂雷云店--基础版",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/goods\/20180409\/93c7115232752884714.png",
				"sell_price":"365.00",
				"activity_info":{
					"productId":"FL001001",
					"skuNo":"FL001001-04",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"1408",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a715bc8d7c76.png"]
			},
			{
				"sku_id":"1000000005",
				"operate_type":2,
				"index":9,
				"type":9,
				"product_num":"",
				"search_name":"店铺标准版",
				"short_name":"高级版",
				"sku_no":"FL001001-06",
				"title":"蜂雷云店--高级版",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/goods\/20180409\/93c7115232752884714.png",
				"sell_price":"3650.00",
				"activity_info":{
					"productId":"FL001001",
					"skuNo":"FL001001-06",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"1405",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a715bc8d7c76.png"]
			},
			{
				"sku_id":"1000000004",
				"operate_type":2,
				"index":10,
				"type":9,
				"product_num":"",
				"search_name":"店铺标准版",
				"short_name":"基础版",
				"sku_no":"FL001001-05",
				"title":"蜂雷云店--标准版",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/goods\/20180409\/93c7115232752884714.png",
				"sell_price":"1800.00",
				"activity_info":{
					"productId":"FL001001",
					"skuNo":"FL001001-05",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"1391",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a715bc8d7c76.png"]
			},
			{
				"sku_id":"1000000006",
				"operate_type":2,
				"index":11,
				"type":9,
				"product_num":"",
				"search_name":"店铺标准版",
				"short_name":"高级版",
				"sku_no":"FL001001-07",
				"title":"蜂雷云店--专业版",
				"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/server\/goods\/20180409\/93c7115232752884714.png",
				"sell_price":"18000.00",
				"activity_info":{
					"productId":"FL001001",
					"skuNo":"FL001001-07",
					"productPrice":"00.00",
					"costPrice":"00.00",
					"activityId":null,
					"activityType":null,
					"title":null,
					"status":"0",
					"isAct":false
				},
				"store_id":"115144354559710",
				"sell_nums":"1379",
				"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I4\/5a715bc8d7c76.png"]
			}]
		}],
		"store_info":{
			"id":"115066910197999",
			"store_name":"邹柯的云店多少",
			"store_desc":"1",
			"bgpath":null,
			"short_number":"258731",
			"invitation_code":"258731",
			"qr_code":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/img\/Qrcode\/I4\/115066910197999.png?v=1521541204",
			"logopath":"http:\/\/img.test.feelee.cc\/\/Public\/Images\/Common\/userLogo.png",
			"qrcode_desc":"蜂雷，赚钱从未如此简单!",
			"url":"http:\/\/feeleeh5.com\/cloud\/advanced?store_id=115066910197999",
			"store_version":"1"
		},
		"list_status":2,
		"shop_decorate_method":{
			"head":"装修秘籍",
			"list":[{
				"title":"1、第壹式：",
				"content":"系统初始会使用“默认样式”，商品默认按照销量从高到低进行排列；"
			},
			{
				"title":"2、第贰式：",
				"content":"点击“选择样式”，即可选择店主精选的商品布局样式；哈哈，前提是有2套或以上的样式可选哦 ^o^"
			},
			{
				"title":"3、第叁式：",
				"content":"点击商品图片，可以更换商品；点击空白区域，可以添加商品；点击“删除”图标，可以删除商品；"
			},
			{
				"title":"4、第肆式：",
				"content":"选择完样式，设置完商品后，那赶紧点击“预览”看看装修成果吧；"
			},
			{
				"title":"5、第伍式：",
				"content":"最终确认无误后，点击右上角的“发布”，即可正式生效；"
			},
			{
				"title":"6、第陆式：",
				"content":"完。"
			}],
			"foot":"若以上6式都已学会，那恭喜你，你可以毕业了，小蜜感到很欣慰；如果还有其他问题，可以联系我们客服小姐姐哦；"
		}
	}
}

```

### 5.5 返回参数

   无
-----------------------
## 6. myHomeStore --- 邹柯

### 6.1 功能描述

旗舰版店铺首页

### 6.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/myHomeStore?  调试参数:{"keywords":"","source":"1","store_type":"other","username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.myHomeStore","type":"1","sort":"","store_id":"115075399495199","page":"1","pageSize":"20","type_id":"1"}

### 6.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| type_id | 否 | int | 要装修商品的类型(1-平台、2-特色)|
| type | 否 | int | 板块类型(0-店主精选、1-全部宝贝、2-热销Top100)|
| sort | 否 | int | 排序字段:type=1时必传(1销量由高到低、2价格由低到高、3价格由高到低)|
| source | 是 | int | 来源(1-H5、2-webApp)|
| store_id | 是 | string | 店铺id|
| store_type | 是 | string | 店铺标识(me本店，其他非本店)|
| keywords | 否 | string | 搜索(商品名称)|
| page | 否 | int | 页码(不传默认1)|
| pageSize | 否 | int | 每页显示条数(不传默认10)|
### 6.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":{
		"store_info":{
			"logopath":"http:\/\/img.test.feelee.cc\/\/Public\/Images\/Common\/userLogo.png",
			"qrcode_desc":"蜂雷，赚钱从未如此简单!",
			"url":"http:\/\/feeleeh5.com\/cloud\/advanced?store_id=",
			"store_version":null
		},
		"goods_info":{
			"plate_id":0,
			"list":[{
				"type":6,
				"isShow":1,
				"sort":1,
				"goods":[{
					"imgs":["http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I9\/P001219\/P001219-xyqsNNNDrC.jpg",
					"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I5\/P002975\/P002975-65BSz8DPmY.jpg",
					"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I5\/P002975\/P002975-409oFe6y5R.jpg",
					"http:\/\/img.test.feelee.cc\/Public\/Uploads\/img\/I9\/P001219\/P001219-JsN1EpDf5p.jpg",
					"http:\/\/img.test.feelee.cc\/Public\/Uploads\/goodsimg\/I9\/5a1e81afa85f2.jpg"],
					"product_id":"P001219",
					"search_name":"无线路由器wifi穿墙 信号放大 覆盖范围广",
					"short_name":"斐讯K2",
					"sku_no":"P001219-01",
					"sku_id":"1002975101",
					"title":"斐讯（PHICOMM）K2 1200M智能双频无线路由器 ",
					"img":"http:\/\/img.test.feelee.cc\/\/Public\/Uploads\/goodsimg\/I0\/5aa8d44648d05.jpg",
					"sell_price":"399.00",
					"sell_nums":"66825",
					"store_id":"115144354559710",
					"activity_info":{
						"productId":"P001219",
						"skuNo":"P001219-01",
						"productPrice":"00.00",
						"costPrice":"00.00",
						"activityId":null,
						"activityType":null,
						"title":null,
						"status":"0",
						"isAct":false
					},
					"type":6,
					"index":1
				}]
			}],
			"foot":{
				"current_page":"1",
				"pagesize":"1",
				"total_page":368
			}
		},
		"is_store_decorate":"1",
		"is_advanced_store_front":"1"
	}
}

```

### 6.5 返回参数

   无
-----------------------
## 7. getHasTeseGoods --- 邹柯

### 7.1 功能描述

判断是否有特色商品

### 7.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/getHasTeseGoods?  调试参数:{"username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.getHasTeseGoods","store_id":"115075399495199"}

### 7.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| store_id | 是 | string | 店铺id|
### 7.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":{
		"list_status":1
	}
}

```

### 7.5 返回参数

   无
-----------------------
## 8. goodsCategory --- 邹柯

### 8.1 功能描述

店铺装修--商品分类

### 8.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/goodsCategory? 调试参数:{"store_id":"115075399495199","username":"17721355485","check_code":"123456","method":"FlagShipShopDecorate.goodsCategory","type_id":"0"}

### 8.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| type_id | 是 | int | 分类类型(0-全部、1-平台、2-特色)|
| store_id | 是 | string | 店铺id|
| source | 是 | int | 来源(1--h5、2--app)|
### 8.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":{
		"categoryInfo":[{
			"id":"2",
			"name":"特色商品",
			"sort":"2",
			"path":"2",
			"child":[{
				"id":"39",
				"name":"摄像头",
				"sort":"5",
				"path":"2\/39",
				"img":null,
				"ad_info":null,
				"child":null
			},
			{
				"id":"38",
				"name":"鼠标垫",
				"sort":"4",
				"path":"2\/38",
				"img":null,
				"ad_info":null,
				"child":null
			},
			{
				"id":"37",
				"name":"耳机",
				"sort":"3",
				"path":"2\/37",
				"img":null,
				"ad_info":null,
				"child":null
			},
			{
				"id":"36",
				"name":"鼠标",
				"sort":"2",
				"path":"2\/36",
				"img":null,
				"ad_info":null,
				"child":null
			},
			{
				"id":"35",
				"name":"键盘",
				"sort":"1",
				"path":"2\/35",
				"img":null,
				"ad_info":null,
				"child":null
			}]
		}]
	}
}

```

### 8.5 返回参数

   无
-----------------------
## 9. getGoodsListByCate --- 邹柯

### 9.1 功能描述

店铺装修--根据分类获取商品列表

### 9.2 请求说明

> 请求方式：POST

> 请求URL：FlagShipShopDecorate/getGoodsListByCate? 调用参数说明:{"method":"FlagShipShopDecorate.getGoodsListByCate","username":"17721355485","check_code":"123456","type_id":"0","sort":"1","keywords":"","cate_type":"1","brand_id":"","page":"1","pagesize":"10","store_id":"115075399495199"}

### 9.3 请求参数

| 参数 | 是否必须 | 类型 | 说明 |
|--------| --------| --------|--------|
| source | 是 | int | 来源(1--h5、2--app)|
| type | 是 | string | 店铺类型--首页进去(other)、我的蜂店进去(me)|
| type_in | 是 | int | 1-搜索进入、分类进入|
| store_id | 是 | string | 店铺id|
| type_id | 是 | int | 分类类型(0-全部、1-平台、2-特色)|
| sort | 否 | int | 排序字段(1销量由高到低、2价格由低到高、3价格由高到低)--不传默认1|
| keywords | 否 | string | 搜索字段(商品名称)|
| cate_type | 是 | string | 商品所属分类id--格式:13,20,24,16|
| brand_id | 否 | string | 品牌id--格式:3,4,5,6|
| page | 否 | int | 页码(不传默认1)|
| pagesize | 否 | int | 每页显示条数(不传默认10)|
### 9.4 返回结果

```json

{
	"status":"0",
	"errorCode":"0",
	"msg":"成功",
	"result":{
		"goods_info":[{
			"product_id":"P000873",
			"brand_id":"3",
			"search_name":null,
			"seascapes":[],
			"img":"",
			"sell_nums":"1",
			"title":"【0元购返399元】斐讯K2 1200M智能双频无线路由器 WIFI穿墙 PSG1218",
			"sku_id":"8032715893",
			"soft_text":null,
			"is_zero_goods":"0",
			"restriction":null,
			"yuding":"1",
			"sku_no":"P0028792",
			"market_price":null,
			"sell_price":"0.01",
			"cost_price":"0.01",
			"product_num":"1",
			"profit":"0.00",
			"spec_name":": : ",
			"store_id":"115075399495199",
			"activity_info":{
				"productPrice":"00.00",
				"costPrice":"00.00",
				"activityId":null,
				"activityType":null,
				"title":null,
				"isAct":false
			},
			"select_status":2
		}],
		"foot":{
			"current_page":"1",
			"pagesize":"10",
			"total_page":1
		},
		"brand_info":[{
			"id":"3",
			"brand_name":"斐讯",
			"list_status":1
		},
		{
			"id":"6",
			"brand_name":"迅捷",
			"list_status":2
		}],
		"cate_info":[{
			"id":"109",
			"name":"斐讯K3C+E1组合套装",
			"list_status":2
		},
		{
			"id":"108",
			"name":"斐讯N1预售",
			"list_status":2
		}]
	}
}

```

### 9.5 返回参数

   无
-----------------------

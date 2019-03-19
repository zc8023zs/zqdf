# 平台B2B店铺采购
## 店铺列表
/{os}/tob/list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| status | 筛选状态 | int | true |推荐=1 好评=2 距离=3|
| lat | 维度 | String | true ||
| lng | 经度 | String | true ||
| search_key | 搜索关键字 | String | true ||
| brand_id | 品牌 | String | true ||
| version_id | 车型 | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "icon":"店铺logo",
                "shop_name":"店铺名称",
                "shop_type":"自营标识",   //直营=1 加盟=2
                "star_num":"好评星级",
                "comment_num":"评论数",
                "distance":"距离",
                "full_address":"地址",
            }
        ]
    }
}
```
## 信息头条

/{os}/tob/top_list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "demand_id":"需求id",
                "note":"信息内容拼接，eg: 出售福睿斯 2015款 前挡风镀膜加热玻璃 10片"
            }
        ]
    }
}
```
## OE码选车

/{os}/tob/add_car_oem

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| oem | oem码 | String | true ||
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
        "brand_id": "品牌",
        "version_id": "车型"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
        ]
    }
}
```
## 发布需求

/{os}/tob/add_demand

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| token | 用户凭证 | String | true ||
| title | 对应车型 | String | true |备注：通过选择拼接，可修改|
| brand_id | 品牌id | String | true ||
| version_id | 车型id | String | true ||
| brand_id | 分类id | String | true ||
| num | 数量 | String | true ||
| note | 描述 | String | true ||
| shop_name | 店铺名称 | String | true ||
| shop_tel | 店铺电话 | String | true ||
| location | 定位地址 | String | true ||
| province | 省 | String | true ||
| city | 市 | String | true ||
| district | 区 | String | true ||
| lat | 维度 | String | false ||
| lng | 经度 | String | false ||
| full_address | 完整地址 | String | false ||   前端可能无法获取经纬度，会将完整地址拼接传入，后台通过地图接口解析经纬度
| demand_type | 类型 | String | true |求购=1 出售= 2|
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
        ]
    }
}
```
## 管理发布列表

/{os}/tob/demand_list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| token | 用户凭证 | String | true ||
| demand_type | 类型 | String | true |求购=1 出售= 2|
| page | 页 | int | true || 
| size | 条 | int | true ||  
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "demand_id":"需求id",
                "title":"标题",
                "num":"数量",
                "location":"位置",
                "create_time":"发布时间"
            }
        ]
    }
}
```
## 修改发布

/{os}/tob/add_demand

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| token | 用户凭证 | String | true ||
| demand_id | 原需求id | String | true ||
| title | 对应车型 | String | true |备注：通过选择拼接，可修改|
| brand_id | 品牌id | String | true ||
| version_id | 车型id | String | true ||
| brand_id | 分类id | String | true ||
| num | 数量 | String | true ||
| note | 描述 | String | true ||
| shop_name | 店铺名称 | String | true ||
| shop_tel | 店铺电话 | String | true ||
| location | 定位地址 | String | true ||
| province | 省 | String | true ||
| city | 市 | String | true ||
| district | 区 | String | true ||
| lat | 维度 | String | false ||
| lng | 经度 | String | false ||
| full_address | 完整地址 | String | false ||   前端可能无法获取经纬度，会将完整地址拼接传入，后台通过地图接口解析经纬度
| demand_type | 类型 | String | true |求购=1 出售= 2|
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
        ]
    }
}
```
## 删除发布

/{os}/tob/del_demand

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| token | 用户凭证 | String | true ||
| demand_id | 原需求id | String | true || 
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
        ]
    }
}
```
## 求购大厅列表

/{os}/tob/all_demand_list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| brand_id | 品牌id | int | false ||  
| version_id | 车型 | String | false ||
| province | 省 | String | false ||
| city | 市 | String | false ||
| district | 区 | String | false ||
| page | 页 | int | true || 
| size | 条 | int | true ||  
返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "demand_id":"需求id",
                "title":"标题",
                "num":"数量",
                "location":"位置",
                "create_time":"发布时间",
                "demand_type": "求购=1 出售= 2"
            }
        ]
    }
}
```
## 求购详情

/{os}/tob/demand_info

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| demand_id | 原需求id | String | true || 

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
        "title":"标题",
        "create_time":"发布时间",
        "version_name":"对应车型",
        "num":"数量",
        "note":"描述",
        "shop_name":"店铺名",
        "shop_tel":"店铺电话",
        "location":"所在地区",
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [ 
        ]
    }
}
```
## 店铺商品列表

/{os}/tob/shop_good_list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| shop_id | 店铺id | String | true || 
| search_key | 搜索关键字 | String | true || 
| page | 页 | int | true || 
| size | 条 | int | true ||  

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
        "shop_name":"店铺名称",
        "full_address":"店铺地址",
        "service_hotline":"店铺电话"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [ 
            {
                "good_id":"商品id",
                "icon":"图标",
                "goods_name":"商品名称"
            }
        ]
    }
}
```
# 采购订单
## 店铺采购订单

/{os}/tob/shop_good_list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| token | 用户凭证 | String | true ||
| status | 状态 | int | true |待商户确认=0 代付款=1 待收货=2 已完成=3 已取消=4|
| page | 页 | int | true || 
| size | 条 | int | true ||  

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [ 
            { 
                "order_id":"订单id",
                "order_sn":"订单号",
                "order_status":"订单状态",
                "goods":[
                    {
                        "goods_thumb":"商品图标",
                        "goods_name":"商品名称",
                        "market_price":"商品价格",
                        "category_name":"商品分类",
                        "goods_number":"购买数量"
                    }
                ],
                "service_hotline":"商家联系电话"
            }
        ]
    }
}
``` 

# 平台B2B店铺采购
## 店铺列表
/{os}/tob/list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| status | 筛选状态 | int | true |推荐=1 好评=2 距离=3|
| lat | 维度 | String | true ||
| lng | 经度 | String | true ||
| search_key | 搜索关键字 | String | true ||
| lng | 经度 | String | true ||
| brand_id | 车型 | String | true ||
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

/{os}/tob/list

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
                "note":""
            }
        ]
    }
}
```
## OE码选车
## 发布需求
## 管理发布
## 修改发布
## 删除发布
## 求购大厅列表
## 求购详情
## 店铺商品列表
# 采购订单
## 店铺采购订单
## 店铺订单详情
# 购物车
##
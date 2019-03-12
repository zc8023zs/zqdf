# 2c商城首页
## 首页banner

/{os}/platform/banners

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
                "img_url":"图片地址"
            }
        ]
    }
}
```
## 首页店铺列表

/{os}/platform/list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| status | 筛选状态 | int | true |推荐=1 好评=2 距离=3|
| lat | 维度 | String | true ||
| lng | 经度 | String | true ||
| search_key | 搜索关键字 | String | true ||

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
## 店铺入驻

/{os}/platform/list

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- | 
| icon | 店铺封面 | String | true || 
| shop_name | 店铺名 | String | true || 
| shop_tel | 手机号 | String | true || 
| province | 省 | String | true || 
| city | 市 | String | true || 
| district | 区 | String | true || 
| lat | 维度 | String | true || 
| lng | 经度 | String | true || 
| address | 详细地址 | String | true || 
| business_license | 营业执照 | String | true || 
| idcard1 | 法人身份证正面 | String | true || 
| idcard2 | 法人身份证反面 | String | true || 

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

# C端登录注册
## 用户注册

/{os}/user/register

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| mobile | 手机号 | String | true ||
| password | 密码 | int | true ||
| veri_code | 图形验证码 | String | true |  |
| invi_code | 手机验证码 | String | true | 123456 |
| invi_key | 手机验证码凭证 | String | true |  |

返回

``` json
{
    "code": 0,
    "msg": "",
    "dataSingle": {
        "token": "wR9rIkaL6aAiqRfMIe4z602e/x30YQN4Yft7nKGyYcc="
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": []
    }
}
```

## 用户登录

/{os}/user/login

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| mobile | 手机号 | String | true ||
| password | 密码 | int | true ||

返回

``` json
{
    "code": 0,
    "msg": "登录成功",
    "dataSingle": {
        "token": "Fs/fyN5jTlV494ue2uzZ2f1OrY7/T2iV0t2UHsomiFI="
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": []
    }
}
```
## 忘记密码

/{os}/user/reset

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| mobile | 手机号 | String | true ||
| password | 密码 | int | true ||
| veri_code | 图形验证码 | String | true |  |
| invi_code | 手机验证码 | String | true | 123456 |
| invi_key | 手机验证码凭证 | String | true |  |

返回

``` json
{
    "code": 0,
    "msg": "修改成功",
    "dataSingle": {
        "token": "Fs/fyN5jTlV494ue2uzZ2f1OrY7/T2iV0t2UHsomiFI="
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": []
    }
}
```
# C端店铺首页
## 用户默认车辆信息

/{os}/user/car_default

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "brand_logo": "品牌logo",
        "brand_name": "品牌名称",
        "displacement": "车系名称",
        "is_default": "是否默认",
        "displacement": "发动机排量",
        "years": "年份",
        "description": "款型",
        "vin": "车辆识别代码"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": []
    }
}
```
## 用户车型列表

/{os}/user/cars

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "car_id": "车辆id",
                "brand_logo": "品牌logo",
                "brand_name": "品牌名称",
                "displacement": "车系名称",
                "is_default": "是否默认",
                "displacement": "发动机排量"
            }
        ]
    }
}
```
## 车型选择-品牌-车型（含热门品牌）

/{os}/user/brands

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "name":"大分类，-ABCDEFG……", //热门取-分类
                "brand_id": "品牌id",
                "brand_logo": "品牌logo",
                "brand_name": "阿斯顿·马丁",
                "children":[
                    {
                        "brand_id": "品牌id",
                        "brand_name": "阿斯顿·马丁",
                        "children":[
                            {
                                "brand_id": "品牌id",
                                "brand_name": "阿斯顿·马丁DB11",
                            }
                        ]
                    }
                ]
            }
        ]
    }
}
```
## 车型选择-排量

/{os}/user/brand_displacements

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| brand_id | 品牌id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "brand_id": "品牌id",
                "version_type_id": "车型配置表",
                "displacement": "排量"
            }
        ]
    }
}
```
## 车型选择-年份

/{os}/user/brand_years

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| brand_id | 品牌id | String | true ||
| displacement_id | 排量-配置表id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "brand_id": "品牌id",
                "displacement_id": "车型配置表排量id",
                "years_id": "车型配置表年份id",
                "years": "年份"
            }
        ]
    }
}
```
## VIN码选车（输入VIN码/图片)

/{os}/user/vins

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| vin_code | vin码 | String | true |不为空，用code解析|
| img_src | vin图片 | String | true |不为空，用img解析|

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                //待定
            }
        ]
    }
}
```
## 店铺详情

/{os}/user/shop_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| shop_id | 店铺id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "brand_logo": "品牌logo",
        "brand_name": "品牌名称",
        "displacement": "车系名称",
        "is_default": "是否默认",
        "displacement": "发动机排量",
        "years": "年份",
        "description": "款型",
        "vin": "车辆识别代码"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": []
    }
}
```
## 店铺评论列表

/{os}/user/shop_comments

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| shop_id | 店铺id | String | true ||
| good_id | 商品id | String | false |为空查所有否则关联商品|

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": { 
        "comment_cnt": "评论数"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "icon": "头像",
                "user_name": "名称",
                "content": "评论内容",
                "add_time": "评论时间", //格式化之后的时间
                "thumb_url":[
                    //缩略图
                ]
            }
        ]
    }
}
```
# 商品
## 店铺玻璃分类

/{os}/user/shop_categorys

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| shop_id | 店铺id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "cat_id": "0",
                "cat_name": "全部",
                "cat_logo": ""
            },
            {
                "cat_id": "分类id",
                "cat_name": "分类名称",
                "cat_logo": "分类logo"
            }
        ]
    }
}
```
## 店铺商品列表

/{os}/user/shop_goods

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| shop_id | 店铺id | String | true ||
| cat_id | 分类id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [ 
            {
                "goods_id":"商品id",
                "goods_thumb":"商品图标",
                "goods_name":"商品名称",
                "market_price":"商品价格"
            }
        ]
    }
}
```
## 商品详情

/{os}/user/shop_goods

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| shop_id | 店铺id | String | true ||
| good_id | 商品id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "goods_id":"商品id", 
        "goods_name":"商品名称",
        "market_price":"商品价格",
        "goods_number":"商品库存",
        "gallery":[
            {
                "img_url":"相册地址", 
                "img_desc":"图片描述"
            }
        ],
        "service_str":"XX本地可提供上门服务", //取店铺注册城市
        "carriage":"配送费",
        "comment_cnt":"评论数",
        "cart_cnt":"购物车数",
        "goods_desc":"商品介绍",
        "other_desc":"包装售后",
        "good_attrs":[
            {
                "attr_name":"标题",
                "attr_value":"值"
            }
        ]
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
## 用户可用优惠券

/{os}/user/good_user_coupon

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||
| good_id | 商品id | String | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "rec_id": "优惠券id",
                "amount": "金额",
                "desc": "满减描述",
                "create_time":"领取时间",
                "expire_time":"过期时间"
            }
        ]
    }
}
```
## 商品实时价格和库存
## 店铺修理厂列表
## 用户收货地址列表
# 购物车
## 购物车列表
## 确认订单详情
## 微信支付
# 个人中心（常规）
## 个人中心首页（含修理厂）
## 个人资料
## 昵称修改
## 换绑手机号
## 客服中心-常见问题
## 投诉举报
## 收货地址详情
## 收货地址编辑
## 收货地址设置默认
## 收货地址删除
## 我的优惠券
## 店铺优惠券领券中心
# 个人中心（挂账）
## 销账明细
## 月销账订单
## 挂账订单列表
## 挂账订单详情
## 挂账订单删除
# 我的订单
## 我的订单列表
## 订单详情
## 取消订单
## 删除订单
## 申请退货
## 售后详情
## 订单评价
# 修理厂中心
## 修理厂中心首页
## 编辑修理厂资料
## 财务管理页面数据
## 申请提现
## 收入明细
## 提现明细
## 银行卡列表
## 解绑银行卡
## 银行卡详情
## 添加银行卡
## 修理厂普通订单
## 修理厂到店技师安装订单
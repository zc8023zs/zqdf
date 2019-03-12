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
## 店铺活动优惠券列表

/{os}/user/good_shop_coupon

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
                "coupon_id": "活动优惠券id",
                "amount": "金额",
                "desc": "满减描述",
                "begin_time":"活动开始时间",
                "end_time":"活动结束时间",
                "have":"是否领取,1=领取 0=未领取"
            }
        ]
    }
}
```
## 店铺活动优惠券领取

/{os}/user/good_shop_coupon

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||
| coupon_id | 活动优惠券id | String | true ||

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
        ]
    }
}
```
## 商品实时价格和库存

/{os}/user/good_price_number

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
        "market_price":"商品价格",
        "number": "实时库存"
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
## 店铺修理厂列表

/{os}/user/good_reapirs

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||
| good_id | 商品id | String | true ||
| lat | 维度 | String | true ||
| lng | 经度 | String | true ||

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
            "user_id": "修理厂id",
            "icon": "头像",
            "is_self": "是否自营",
            "user_name":"修理厂名称",
            "addr":"完整地址",
            "distance":"距离（千米）"
        ]
    }
}
```
## 用户收货地址列表

/{os}/user/good_user_addrs

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
                "address_id": "收货地址id",
                "consignee":"收货人姓名",
                "addr":"完整地址",
                "mobile":"收货人电话"
            }
        ]
    }
}
```
## 加入购物车

/{os}/user/good_carts_add

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||
| good_id | 商品id | String | true ||
| addr_method | 配送方式 | String | true |配送至：修理厂/其它地址|
| addr_id | 地址id | String | true ||
| installer | 地址id | String | true |服务方式：安装/不安装|

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
        ]
    }
}
```
# 购物车
## 购物车列表

/{os}/user/good_user_carts

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
                "rec_id":"购物车id",
                "goods_id":"商品id",
                "goods_thumb":"商品图标",
                "goods_name":"商品名称",
                "market_price":"商品价格",
                "category_name":"商品分类",
                "goods_number":"购买数量"
            }
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
## 提交订单

/{os}/user/good_order

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| addrs | 收货地址 | String | true || 
| coupon_id | 优惠券 | String | true || 
| goods | 商品ids | String | true || 

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "order_id":"订单号",
        "order_price":"订单金额"
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
## 支付

/{os}/user/good_user_buy

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| type  | 支付类型 | String | true |0微信| 
| order_id  | 订单ID | String | true ||  

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "nonce_str": "KpdSOiO1pWDAeQ5P", //订单号
        "payMoney": "0.01", //支付金额
        "paySign": "4B36BD9E9811573DBBDD8FEE828C8ECB", //签名
        "packages":"prepay_id=wx08163851926528a6c95bd7fa1688041404",  //包名
        "prepay_id": "wx08163851926528a6c95bd7fa1688041404"
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
# 个人中心（常规）

/{os}/user/user_index

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
        "icon":"头像",
        "user_name":"名称",
        "unpay_cnt":"待付款数",
        "uninstall_cnt":"待安装数",
        "uncomment_cnt":"待评价数",
        "after_sale_cnt":"退款/售后数",
        "is_credit": "是否挂账", //0=否 1=是
        "unpay_credit":"未销账金额",
        "sum_order":"总下单金额",
        "credit":"已销账金额"
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
## 个人资料

/{os}/user/user_info

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
        "icon":"头像",
        "user_name":"名称",
        "sex":"性别", //0=未设置 1=男 2=女 
        "user_mobile":"手机号",
        "province":"省",
        "city":"市",
        "district":"地区",
        "full_address":"完整地址"
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
## 修改头像

/{os}/user/user_update_icon

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| icon | 新头像 | String | true ||  

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
        ]
    }
}
``` 
## 昵称修改

/{os}/user/user_update_user_name

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| user_name | 新头像 | String | true ||  

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
        ]
    }
}
``` 
## 换绑手机号

/{os}/user/user_update_mobile

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| mobile | 新手机号 | String | true ||  
| sms_key | 手机号凭证 | String | true ||  

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
        ]
    }
}
``` 
## 客服中心-常见问题

/{os}/user/user_questions

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
                "id":"问题标题",
                "title":"标题",
                "content":"内容"
            }
        ]
    }
}
``` 
## 投诉举报

/{os}/user/user_complain

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||  
| content | 投诉内容 | String | true ||  

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
        ]
    }
}
``` 
## 收货地址详情

/{os}/user/user_address_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||  
| address_id | 收货地址id | String | true ||  

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {  
        "address_id":"是收获地址id",
        "consignee":"收货人姓名",
        "mobile":"手机号码",
        "province":"收货-省",
        "city":"收货-市",
        "district":"收货-区",
        "full_address":"详细地址",
        "is_default":"是否默认",
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
## 收货地址编辑

/{os}/user/user_address_update

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||  
| address_id | 收货地址id | String | true ||  

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {  
        "address_id":"是收获地址id",
        "consignee":"收货人姓名",
        "mobile":"手机号码",
        "province":"收货-省",
        "city":"收货-市",
        "district":"收货-区",
        "full_address":"详细地址",
        "is_default":"是否默认",
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
## 收货地址设置默认

/{os}/user/user_address_default

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||  
| address_id | 收货地址id | String | true ||  
| is_default | 是否默认 | String | true |1=是 0=否| 

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
        ]
    }
}
``` 
## 收货地址删除

/{os}/user/user_address_del

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||  
| address_id | 收货地址id | String | true ||   

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
        ]
    }
}
``` 
## 设置页面数据

/{os}/user/user_setting_info

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
        "url1":"相关协议",
        "url2":"免责声明"
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
## 修改密码

/{os}/user/user_setting_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |  
| token | 用户凭证 | String | true ||    
| old_pwd | 旧密码 | String | true ||   
| new_pwd | 新密码 | String | true ||   

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
        ]
    }
}
``` 
## 我的优惠券

/{os}/user/user_coupon_list

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||
| status | 状态 | String | true |全部=0 未使用=1 已使用=2 已过期=3（含时间已过期）|

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
# 个人中心（挂账）
见上面的个人中心
## 销账明细

/{os}/user/user_credit_del_list

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| page | 页 | int | true || 
| size | 条 | int | true ||  

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
                "title": "标题",
                "amount": "销账金额", 
                "cancel_time":"销账时间"
            }
        ]
    }
}
```
## 月销账订单

/{os}/user/user_credit_del_list_month

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| page | 页 | int | true || 
| size | 条 | int | true ||  

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
                "order_sn": "订单编号",
                "good_num": "商品数", 
                "money_paid":"订单金额",
                "add_time":"下单时间"
            }
        ]
    }
}
```
## 挂账订单列表

/{os}/user/user_credit_order_list

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| page | 页 | int | true || 
| size | 条 | int | true ||  
| type | 类别 | int | true |全部=-1 未销账=0 已销账=1|  

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
                "order_id": "订单id",
                "order_sn": "订单编号",
                "credit": "销账状态", 
                "good_num": "商品数", 
                "order_amount":"应付款金额",
                "money_paid":"付款金额",
                "bonus":"红包金额",
                "goods":[
                    {  
                        "goods_thumb":"商品图标",
                        "goods_name":"商品名称",
                        "market_price":"商品价格",
                        "category_name":"商品分类",
                        "goods_number":"购买数量"
                    }
                ]
            }
        ]
    }
}
```
## 挂账订单详情

/{os}/user/user_credit_order_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "order_id": "订单id",
        "is_credit_del":"销账状态 0=未销账 1=成功",
        "consignee":"收货人姓名",
        "mobile":"收货人电话",
        "full_address":"完整收货地址",
        "repair_name":"修理厂名称",
        "order_sn":"订单号",
        "order_amount":"应付款金额",
        "money_paid":"付款金额",
        "bonus":"红包金额",
        "add_time":"下单时间"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [ 
            {
                "goods_thumb":"商品图标",
                "goods_name":"商品名称",
                "market_price":"商品价格",
                "category_name":"商品分类",
                "goods_number":"购买数量"
            }
        ]
    }
}
```
## 挂账订单删除(订单状态修改成已删除)

/{os}/user/user_credit_order_del

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||

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
        ]
    }
}
```
# 我的订单
## 我的订单列表

/{os}/user/user_order_list

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| status | 状态 | int | true |全部=0 代付款=1 待安装=2 已完成=3 已取消=4|

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
                "order_id": "订单id",
                "order_sn": "订单号",
                "add_time": "下单时间",
                "status_name": "状态名称",
                "order_amount":"应付款金额",
                "money_paid":"付款金额",
                "bonus":"红包金额",
                "goods":[
                    {  
                        "goods_thumb":"商品图标",
                        "goods_name":"商品名称",
                        "market_price":"商品价格",
                        "category_name":"商品分类",
                        "goods_number":"购买数量"
                    }
                ]
            }
        ]
    }
}
```
## 订单详情

/{os}/user/user_order_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": { 
        "order_id":"订单id",
        "status":"订单状态",
        "status_txt":"订单状态文字",
        "consignee":"收件人姓名",
        "mobile":"收件人手机号",
        "full_address":"详细地址",
        "repair_name":"修理厂名称", //修理厂名称 判空展示
        "order_amount":"应付款金额",
        "money_paid":"付款金额",
        "bonus":"红包金额",
        "add_time": "下单时间",
        "pay_time": "付款时间"
    },
    "dataArray": {
        "pageSize": 0,
        "pageIndex": 0,
        "pageCount": 0,
        "dataCount": 0,
        "dataList": [
            {
                "goods_thumb":"商品图标",
                "goods_name":"商品名称",
                "market_price":"商品价格",
                "category_name":"商品分类",
                "goods_number":"购买数量"
            }
        ]
    }
}
```
## 取消订单

/{os}/user/user_order_cancel

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||
| note | 取消原因 | String | true ||

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
        ]
    }
}
```
## 删除订单

/{os}/user/user_order_del

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||

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
        ]
    }
}
```
## 售后申请列表（已完成订单）

/{os}/user/user_order_return_list

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| status | 状态 | String | true |售后申请=0 处理中=1 申请记录=2| 

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
                "order_id":"订单id",
                "goods":[
                    { 
                        "goods_thumb":"商品图标",
                        "goods_name":"商品名称",
                        "market_price":"商品价格",
                        "category_name":"商品分类",
                        "goods_number":"购买数量"
                    }
                ],
                "can_return":"是否可售后"  //是否可申请售后，通过店铺配置售后过期时间确认
            }
        ]
    }
}
``` 
## 售后评价列表 

/{os}/user/user_order_return_comment

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
                "comment_rank":"星级", 
                "content":"评论内容", 
                "imgs":"评论相册"
            }
        ]
    }
}
``` 
## 申请退货

/{os}/user/user_order_return

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||
| note1 | 申请理由 | String | true ||
| note2 | 详细说明 | String | true ||
| img[] | 上传图片 | String[] | true ||

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
        ]
    }
}
```
# 退款/售后详情

/{os}/user/user_order_return_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {  
        "order_status":"售后状态",
        "goods":[
            { 
                "goods_thumb":"商品图标",
                "goods_name":"商品名称",
                "market_price":"商品价格",
                "category_name":"商品分类",
                "goods_number":"购买数量"
            }
        ],
        "cancel_time":"售后申请时间", 
        "cancel_sn":"售后编号", 
        "cancel_time":"申请理由", 
        "cancel_time":"详细说明"
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
## 订单/售后评价

/{os}/user/user_order_comment

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| order_id | 订单id | int | true ||
| comment_rank | 评价星级 | int | true ||
| content | 评论内容 | String | true ||
| img[] | 评论图片 | String[] | true ||
| type | 评论类别 | int| true |订单评论=1 售后评论=3 技师评论=2|

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
        ]
    }
}
```
# 修理厂中心
## 修理厂中心首页

/{os}/user/user_repair_index

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
        "icon":"头像",
        "user_name":"修理厂名称",
        "full_address":"修理厂地址",
        "all_amount":"累计交易金额",
        "all_num":"累计完成订单"
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
## 编辑修理厂资料

/{os}/user/user_repair_update_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true || 
| icon | 修理厂头像 | String | true || 
| shop_name | 店铺名称 | String | true || 
| shop_tel | 店铺电话 | String | true || 
| lat | 定位维度 | String | true || 
| lng | 定位经度 | String | true || 
| address | 详细地址 | String | true || 
| business_license | 营业执照 | String | true || 
| idcard1 | 法人身份证正面 | String | true || 
| idcard2 | 法人身份证反面 | String | true || 

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
        ]
    }
}
```
## 财务管理页面数据

/{os}/user/user_repair_update_info

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
        "can_amount":"可提现金额",
        "all_amount":"累计金额",
        "done_amount":"已提金额"
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
## 银行卡列表

/{os}/user/user_cards

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
                "bank_name":"银行名称",
                "card_no":"银行卡号",
                "card_id":"银行卡id",
            }
        ]
    }
}
```
## 解绑银行卡

/{os}/user/user_card_del

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| card_id | 银行卡id | int | true ||  

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
        ]
    }
}
```
## 银行卡详情

/{os}/user/user_card_info

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| card_id | 银行卡id | int | true ||  

返回

``` json
{
    "code": 0,
    "msg": "成功",
    "dataSingle": {
        "bank_name":"银行名称",
        "card_no":"银行卡号",
        "card_id":"银行卡id",
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
## 添加银行卡

/{os}/user/user_card_add

输入参数

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| token | 用户凭证 | String | true ||  
| card_no | 银行卡姓名 | int | true ||  
| user_name | 持卡人姓名 | int | true ||  

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
        ]
    }
}
```
## 申请提现
## 收入明细
## 提现明细
## 修理厂普通订单
## 修理厂到店技师安装订单
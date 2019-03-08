# C端登录注册
## 用户注册

/{os}/user/register

| 参数名 | 描述 | 类型 | 必填 | 默认 | 说明 |
| --------- | ---------- | ------ | ---- | ---- | --------------------------------------------- |
| mobile | 手机号 | String | true ||
| password | 密码 | int | true ||
| veri_code | 验证码 | String | true |  |
| invi_code | 验证码 | String | true | 123456 |

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
# C端店铺首页
## 用户当前爱车（车型详情）
## 用户车型列表
## 车型选择-品牌-车型-排量-年份（含热门品牌）
## VIN码选车（输入VIN码/图片)
## 店铺详情
## 店铺评论列表
# 商品
## 店铺玻璃分类
## 店铺商品列表
## 商品详情
## 用户可用优惠券
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
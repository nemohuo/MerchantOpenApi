First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

**接口地址 : /merchantapi/pushdeliverymsg**

**请求方法 :POST**

**请求参数**

参数名 | 必填 | 类型 | 描述 | 样例
------------ | ------------ | ------------ | ------------ | ------------
timeStamp | 必填 | int | 时间戳 | 1478589796
appId | 必填 | text | APP ID | test
sign | 必填 | text | 签名 | E5F7D96195B17794857A88B6952F5169
param | 必填 | json | 物流信息列表 | 支持多个，详细请看"param字段参数"

**param字段参数**

参数名 | 必填 | 类型 | 描述 | 样例
------------ | ------------ | ------------ | ------------ | ------------
orderId | 必填 | int | 平台订单编号 | 2147483649
deliveryComCode | 必填 | text | 物流公司编码 | huitongkuaidi
deliveryNo | 必填 |text | 物流单号 | 2147483649214
type | 选填 | int | 推送类型 0(默认):添加物流单号 1:重置物流单号 | 0

**返回数据**

参数名 | 必填  | 类型 | 描述 | 样例
------------ | ------------ | ------------ | ------------ | ------------
success | 必填 | int | 推送成功的数量 |  |
failed | 必填 | int | 推送失败的数量 |  |

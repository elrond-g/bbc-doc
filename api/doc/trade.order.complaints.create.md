# ONEX B2B2C 商城API文档

## 交易相关API

### 买家对不满意订单发起投诉(trade.order.complaints.create)

* 系统参数

| *字段* | *标题* | *数据类型* | *验证条件* | *示例值* | *默认值* | *详细说明* |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| method | API的方法名 | string | required | trade.get | null | 标识请求的是哪个API |
| timestamp | 请求时间 | unix时间戳 | required , numeric , > time()-300 | 1440596821 | null | 标识API请求的发起时间，如果超时300秒则拒绝请求 |
| format | 返回数据格式 | string | required | json | json | 返回数据是json格式的，目前只支持json |
| v | 版本号 | string | required | v1 | null | 标识该接口的版本 |
| sign_type | 签名方式 | string | required | MD5 | null | 标识签名算法 |
| sign | 签名 | string | required | AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA | null | 数据签名，32位长度16进制数字 |


* 业务参数

| *字段* | *标题* | *数据类型* | *验证条件* | *示例值* | *默认值* | *详细说明* |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| oid |  | int | required | 1506181717250001 |  | 投诉子订单号 |
| tel |  | string | required | 13918987654 |  | 投诉人联系方式 |
| image_url |  | string |  |  |  | 投诉图片凭证URL，最多5张图片，URL用逗号隔开 |
| complaints_type |  | string | required | 售后问题 |  | 投诉类型 |
| content |  | string | required,min:5,max:300 | 商家描述可以随时退款，现在说不能退 |  | 投诉问题的具体描述 |


*返回内容示例

```



```

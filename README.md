# 发财付
发财付是一个第三方支付平台，类似于支付宝、证通等。

## 接口
1. 后台签约接口
2. 后台解约接口
3. 单笔代扣接口
4. 单笔代付接口
5. 交易查询接口
6. 账户余额查询接口

## 特点
1. 为商户提供了一个管理平台，商户可在此平台上进行一些个性设置。
2. 通讯共有2种模式，加密模式和调试模式，调试模式不用加密签名，商户可自行在平台上配置。
3. 商户可在平台上配置通讯编码，默认为UTF-8编码。
4. 商户可在平台上配置是否需要对账文件，以及在什么时间需要哪些交易的对账。
5. 商户可在平台上配置单笔限额和日累计限额。
6. 由于这是一个虚拟的交易平台，所以本平台规定，交易金额的后两位为错误码的后两位，可供商户进行多样化测试。

## 清算对账
### 普通对账
在T+1日凌晨1点生成对账文件，并主动推送给商户，商户可自行在此平台配置自己的ftp地址。

### 基金公司对账
一般基金公司都是下午三点收市，下午三点多就需要对账，所以本平台会根据商户交易时送的“清算日期”来生成对账文件，  
并在15::20生成对账文件并主动推送给商户。

## 生产上线
商户使用“公测商户”进行联调完毕后，可申请一个特有的商户号。暂不支持在线申请，后面可能会增加此功能。

## 最新接口文档
[发财付平台接口规范.docx](http://kangyonggan.com:8888/downloads/发财付平台接口规范.docx)

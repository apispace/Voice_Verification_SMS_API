# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=yuyinyanzhengma) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：
- Java(OK HTTP)
- HTTP
- cURL
- 微信小程序
- PHP(pecl_http)、PHP(cURL)
- Python(http.client)、Python(Requests)
- JavaScript(Jquery AJAX)、JavaScript(XHR)
- NodeJS(Native)、NodeJS(Request)
- Ruby(Net:Http)
- Shell(Httpie)、Shell(cUrl)

# 语音验证码短信
语音验证码服务，拨打电话告知用户验证码，实现信息验证。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/sms-voice/introduction](https://www.apispace.com/eolink/api/sms-voice/introduction?utm_source=github&utm_term=yuyinyanzhengma) 申请API服务**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/sms-voice/guidence/](https://www.apispace.com/eolink/api/sms-voice/guidence/?utm_source=github&utm_term=yuyinyanzhengma)

### 应用场景

语音验证码是一种非常安全且易于使用的认证方式，它能够有效防止恶意攻击和身份盗用的行为，以保护用户的资料安全。

语音验证码的使用场景分布广泛，主要用于多种网络服务和网站的验证和认证活动。
1.  #### 银行和金融机构
在开展金融服务时，为了保证身份资料的真实性，会使用语音验证码来进行身份认证。

2.  #### 电商平台
在进行账户注册或实名认证的过程中，电商平台会使用语音验证码来加强安全性。

3.  #### 政府机构
政府机构在开展电子政务系统的维护和安全认证工作时，也会使用语音验证码。

4.  #### 社交网络
社交网络在用户注册或登录账户时，会使用语音验证码来验证真实身份。

5.  #### 网络游戏
在网络游戏中，用户在登录游戏账号时，也可以使用语音验证码作为一种认证方式。

### 使用须知

接听成功扣费，接听不成功不扣费。

### Python(Requests) 调用代码示例

```
import requests

url = "https://eolink.o.apispace.com/sms-voice/voice-code"

payload = {"mobile":"","content":66666,"allowedCallTime":30,"transData":""}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":"application/x-www-form-urlencoded"
}

response=requests.request("POST", url, data=payload, headers=headers)

print(response.text)

```

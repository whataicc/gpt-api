# 高效的Open AI、Midjourney API代理、Claude代理、Suno代理等供应商


神马聚合中转API是一个高效的Open AI、Midjourney API代理、Claude代理、Suno代理等供应商
我们致力于提供优质的 API 接入服务，让您可以轻松集成先进的AI模型至您的产品和服务。通过 API 综合管理平台，无缝整合OpenAl最尖端的人工智能模型。借助我们可靠且易于使用的API解决方案，升级您的产品与服务。

[![神马聚合中转API_低价gpt_中转api_好用稳定的GPT代理_claude中转api_Midjourney代理_Suno代理_Luma代理](https://pic2.imgdd.cc/item/68c78cabfcdff65483faea2a.jpg "神马聚合中转API_低价gpt_中转api_好用稳定的GPT代理_claude中转api_Midjourney代理_Suno代理_Luma代理")](https://api.whatai.cc)

让您能够轻松一站式接入各种 AI 服务

价格优惠，仅需 2 元即可购买1美刀额度

注册即送0.2刀，不限时间，按量计费

明细可查，每一笔消耗都公开透明

支持 OpenAI 官方所有模型，以及其他市面上常见模型！

注意！我们的价格是 2 = 1 刀额度！！

只需设置模型名，即可开始使用模型！

模型名称即下面的模型列中的内容

除3.5、4.0模型以外，其他模型价格与官方完全一致(注意我们是2元人民币买1刀)


# 这里是使用教程  

### 新用户注册赠送 0.2 刀额度，前往令牌页复制令牌，在聊天页设置中填入即可体验！



### 目录

```
· 分组区别
· 网站使用教程
  · GPT接入教程
  · Midjourney 接入教程
· 常见项目配置方式
· 常见问题
```

<br/>


## 分组区别
![截图](https://s3.bmp.ovh/imgs/2024/05/07/a20f70b11e00b855.png)  



## 网站使用教程

🔥 均为高速回复渠道非低价普通渠道

💰 为方便计费，一个账号通用所有模型，兑换比例固定为 2 元兑换 1美金
其中GPT-4全模型（含32K、Dalle3）后台为官方计费倍率 2 倍，相当于4元兑换1美金（约等于官方的2.4折） 

后台日志计费规则解析：假如提示是2000，补全是1000，使用的gpt-4，则您后台的扣费公式=(2000/1000)x0.03（提问价格）+(1000/1000)x0.06（回答价格）=$0.12   


### GPT接入教程

1. 注册账号，免费体验，注册即送0.2美金额度，1刀起充
2. 前往[令牌页](/token)，添加令牌
3. 修改应用 BASE_URL为中转接口调用地址： https://api.whatai.cc  设置 API Key 为添加的令牌

不同的客户端需要填写不同的BASE_URL, 请尝试如下地址  
https://api.whatai.cc  
https://api.whatai.cc/v1  
https://api.whatai.cc/v1/chat/completions  

模型名在[首页](/) -> 支持模型中的第一列 模型 中   
可在[聊天页](/chat) 进行测试或使用

<br/>

### Midjourney 接入教程

Midiourney-Proxy主机：https://api.whatai.cc

Midiourney-Proxy Secret ：自己后台生成的令牌

同时支持 Mid journey proxy Plus 以及 Mid journey proxy 接口协议

上面为MJ Proxy快捷接入方式，如果你的项目不支持以上方式，请点击查看[接入文档](https://gpt-best.apifox.cn/doc-3530863)

以下参数均可在令牌设置中进行设置  
切换 MJ mode: 

1. 通过 URL 路径切换   
默认 /mj 是 fast mode   
/mj-fast/mj 是 fast mode   
/mj-turbo/mj 是 turbo mode   
/mj-relax/mj 是 relax mode   
例如： https://api.whatai.cc/mj-turbo/mj/submit/imagine
2. prompt 中通过 mj 参数指定： --relax\--fast\--turbo

切换 MJ 返回的图片地址：
1. 通过 URL 路径切换   
默认 /mj 是管理员设置默认方式    
/mj-{mode}-relay/mj 是使用服务转发地址，图片国内访问较快   
/mj-{mode}-origin/mj 是使用discord 原地址，图片国外访问很快   
/mj-{mode}-proxy/mj 是使用管理员设置的代理地址，图片国内访问较快  
例如： https://api.whatai.cc/mj-turbo-relay/mj/submit/imagine


**价格表**

|Mode 模式|类型1端点(根据mode调整价格)|类型2端点 (固定价格)|类型3端点(免费)|
|--|--|--|--|
|Relax|0.12/次|0.07/次|0/次|
|Fast|0.2/次|0.07/次|0/次|
|Turbo|0.4/次|0.07/次|0/次|

<br/>

类型1端点：

1. 类型 1 端点包括：Imagine/Variation/Outpaint/Pan/Blend/Inpaint/Upscale 2x/Upscale 4x/PicReader/Reroll
   1. ```
      中文释义：绘图/变换/变焦/焦点移动/混图/局部重绘/放大2倍/放大4倍/图生文后生成图片/重新生成
      ```
2. 类型 2 端点包括：Upscale/Describe/PicReaderRetry/FaceSwap/Shorten
   1. ```
      中文释义：放大/图生文/图生文重新生成/换脸/prompt分析
      ```
3. 类型 3 端点包括：Fetch/ListByIDs/Modal/Seed
   1. ```
      中文释义：获取单个任务进度/批量获取任务/确认提交弹窗任务/获取Seed
      ```

<br/>



## 常见项目配置方式

### **python openai官方库（使用AutoGPT，langchain等）**

示例代码请参考[demo.py](https://api.whatai.cc/demo.py)

***方法一***

```python
import openai
openai.api_base = "https://api.whatai.cc/v1"
```

***方法二（方法一不起作用用这个）***

修改环境变量OPENAI_API_BASE，各个系统怎么改环境变量请自行搜索，修改环境变量后不起作用请重启系统。

```sh
OPENAI_API_BASE=https://api.whatai.cc/v1
```


### **开源gpt_academic**

找到`config.py`文件中的`API_URL_REDIRECT`配置并修改为以下内容：

```python
API_URL_REDIRECT = {"https://api.openai.com/v1/chat/completions": "https://api.whatai.cc/v1/chat/completions"}
```


### **ChatBox(推荐使用)**

ChatGPT开源桌面应用，支持全部桌面平台。

下载链接：https://github.com/Bin-Huang/chatbox/releases

使用方法：如图在设置中填入购买的密钥，并将代理设置为`https://api.whatai.cc`即可

![](https://pic.imgdb.cn/item/66da6b49d9c307b7e9b93284.png)


### **浏览器插件ChatGPT Sidebar**

官网链接：https://chatgpt-sidebar.com/

安装好插件后进入设置页面，如图所示修改设置，将url修改为 `https://api.whatai.cc` 。


![](https://pic.imgdb.cn/item/66da63e0d9c307b7e9b1a111.png)


### **Jetbrains插件ChatGPT - Easycode**

![](https://pic.imgdb.cn/item/66da6604d9c307b7e9b582fd.png)

安装好插件后在Settings > Tools > OpenAI > GPT 3.5 Turbo中如图所示配置好插件，重点要将Server Settings 修改为 `https://api.whatai.cc/v1/chat/completions` 。并勾选Customize Server。


![](https://pic.imgdb.cn/item/66da642ed9c307b7e9b295cd.png)


### **VSCode插件Code GPT**


![](https://pic.imgdb.cn/item/66da644cd9c307b7e9b2eea8.png")

这个插件修改Host相对麻烦一些，需要修改源码才可以使用。

1. 安装插件。安装好后按Ctrl+Shift+P，弹出框中输入Open Extensions Floder
![](https://pic.imgdb.cn/item/66da64f9d9c307b7e9b4b8f9.png)
1. 点击Extensions: Open Extensions Floder，这将打开插件目录，找到Code GPT的文件夹。
![](https://pic.imgdb.cn/item/66da650ed9c307b7e9b4c988.png)
1. 打开后进入打开文件./src/clients/openai_client.js，搜索文件中的api.openai.com，并替换为 `api.whatai.cc`。保存文件。
![](https://pic.imgdb.cn/item/66da652fd9c307b7e9b4e10d.png)
1. 再次回到vscode，按Ctrl+Shift+P，弹出框中输入CodeGPT: Set API KEY，点击CodeGPT: Set API KEY。然后将购买的Key输入进去即可。
![](https://pic.imgdb.cn/item/66da652fd9c307b7e9b4e10d.png)
1. 以上步骤完成后，重启VSCode

- 其他VSCode插件类似。

### **Raycast 插件 ChatGPT（推荐使用）**

1. 在 Raycast Store 中找到 ChatGPT 插件，并按照提示安装：
![](https://pic.imgdb.cn/item/66da657fd9c307b7e9b51aec.png)
2. 安装完成后在该插件配置中的 `API Key` 中填入我们的API Key，以及选中 `Change API Endpoint`，并在 `API Endpoint` 中填入 `https://api.whatai.cc/v1`

![](https://pic.imgdb.cn/item/66da6594d9c307b7e9b529e9.png)
![](https://pic.imgdb.cn/item/66da65bbd9c307b7e9b54be2.png)

1. 🍺 enjoy it~  
 
![](https://pic.imgdb.cn/item/66da65dbd9c307b7e9b56670.gif)



## 常见问题

Q：切换到了GPT-4，询问它是不是GPT-4，为什么回答不是？

A：首先如果你问GPT-4：你是不是GPT4？它大概率会回答：我是OpenAI的GPT-3 模型，目前还没有GPT-4。之所以会这样，是因为OpenAI开放给API调用的GPT-4，训练数据都是2021年9月之前的。模型训练好之后，如果不重新训练，并不会自动更新里面的知识，这就好像我问2021年的你2023年第一顿饭你吃了什么，答案一定是错的。

Q：为什么ChatGPT Plus的GPT-4回答能回答出自己是GPT-4？

A：简单来说，ChatGPT Plus使用的模型版本和开放给API的并不一样，作为内部版本，很大可能会用更新的数据去训练，甚至是实时数据训练。虽然都叫GPT-4，但给出的答案不同，因为训练数据不同。

Q：那我如何去判断他是否是GPT-4模型

A：可使用以下逻辑性问题进行测试 问题 ： 鲁迅和周树人是什么关系 GPT-3.5：鲁迅和周树人是两个不同的人 GPT-4：鲁迅和周树人是同一个人

Q：无法登录？

A：请确保用户名填写正确，不要填写邮箱地址，是填写你注册时候的用户名，如遇到登录问题无法自行解决，请联系客服，第一时间为您处理

Q：为什么请求后没吐字没补全 token  

A：有以下可能  
1. 快吐字了，客户端断开连接  
2. tools call 或 function call  
3. openai 直接返回[Done]，一般是政策安全相关拒绝回答，需要结合返回的 finish_reason或内容进行判断  
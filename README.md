# ChatGPT-website

## 介绍

简易版 `ChatGPT` 网站，拿来即用，适合小白，让你十分钟搭建属于自己的 `ChatGPT` 问答机器人！


## 使用说明

1. 本项目后端用 `flask` 快速搭建，可使用宝塔面板中的python项目管理器快速部署！

2. 本项目支持 `GPT-3.5-turbo` 和 `GPT-4`，支持记录上下文实现连续对话！

3. 本项目支持流式响应，`markdown` 实时转换为 `html`！

4. 由于 `OpenAI` 的 `api` 地区限制问题, 使用现有开源 `api` 代理，则只需在 `settings.py` 配置文件中加入自己的 `OpenAI`  的 `api key` 即可，然后部署到大陆服务器就行！如有条件部署到国外服务器，请使用 `settings.py` 配置文件中的 `OpenAI` 官方 `api` 接口。

## 部署教程

这里有三种方式：

 1. 有自己的服务器，请看：[https://docs.qq.com/doc/DZktaamVkSXlZenFW](https://docs.qq.com/doc/DZktaamVkSXlZenFW)
 2. 无自己的服务器（零成本部署），请看：[https://github.com/Aniuyyds/ChatGPT-website](https://github.com/Aniuyyds/ChatGPT-website)
 3. 可使用`github pages` 或者 `Vercel` 部署的纯前端静态版本（零成本部署）：https://gitee.com/aniu-666/chat-gpt-website/tree/web/

三种部署方式说明：

方式 | 说明
----- | -----
方式一: 有自己的服务器|如果服务器在国内，则要使用代理`api`，且只能用`ip`访问，不能绑定域名，因为`gpt`服务备案无法审核通过；如果有国外服务器，那最好，使用`openai`官方`api`就行，也可绑定域名！
方式二：无自己的服务器|使用`render`云平台零成本部署`flask`项目，只需`fork` `github`镜像仓库即可，具体请看上面部署教程里的链接，缺点是平台限制最大只能流式响应30秒，但不影响，输入“继续”让 chatgpt 继续输出就行！
方式三：纯前端静态版本|功能较方式一和方式二少一点，且是纯静态，因此网络请求是本地浏览器发送的，只能使用代理`api`，一旦代理`api`不能用了，就不能用了。

我比较推荐使用方式一的国外服务器，但国外服务器价格昂贵，香港和台湾的服务器也行，可以不用备案绑定域名，需要注意的是这两个地方也不能访问`openai`官方`api`，因此`settings.py`中要使用代理`api`。
白嫖党可以使用方式二，只不过流式响应30秒，体验较方式一差点。
方式三也没有流式响应时间限制，缺点是容易暴露`apikey`。

如实在看教程部署不了，可进群联系作者花点小钱代为搭建！

## 注意

1. 开发不易，拒绝白嫖，如果此小项目帮助到了您，希望能得到您的 `star` ！
2. 页面可任各位修改，希望留下项目地址，为此项目吸引更多的 `star` !
3. 项目使用的开源代理：[https://github.com/geekr-dev/openai-proxy](https://github.com/geekr-dev/openai-proxy) ，点个 `star` 支持作者
4. 此项目适合小白，主打简洁，可不断完善！
5. 对于项目如有疑问，可加下面 `QQ` 群交流！


## 项目效果

### PC端

<table>
    <tr>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E7%94%B5%E8%84%91%E7%AB%AF%E5%9B%BE%E7%89%87%E4%B8%80.png" width="400">图1</td>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E7%94%B5%E8%84%91%E7%AB%AF%E5%9B%BE%E7%89%87%E4%BA%8C.png" width="400">图2</td>
    </tr>
    <tr>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E7%94%B5%E8%84%91%E7%AB%AF%E5%9B%BE%E7%89%87%E4%B8%89.png" width="400">图3</td>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E7%94%B5%E8%84%91%E7%AB%AF%E5%9B%BE%E7%89%87%E5%9B%9B.png" width="400">图4</td>
    </tr>
</table>

### 手机端

<table>
    <tr>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E6%89%8B%E6%9C%BA%E7%AB%AF%E5%9B%BE%E4%B8%80.png" width="400">图1</td>
        <td align="center"><img src="./%E9%A1%B9%E7%9B%AE%E7%A4%BA%E4%BE%8B%E5%9B%BE/%E6%89%8B%E6%9C%BA%E7%AB%AF%E5%9B%BE%E4%BA%8C.png" width="400">图2</td>
    </tr>
</table>

## 更新日志

### 23 年 5.12 日更新

 1. 可选多种页面主题。
 2. 可在本地保存自己的 `api key` 使用。如果本地不输入 `api key`，则默认使用 `settings.py` 配置文件中的 `api key`。
 3. 可在本地保存历史对话记录，即页面刷新不会消失，默认关闭，可在页面设置中开启。
 4. 可选择是否开启上下文连续对话，默认开启，可在页面设置中关闭。
 5. 添加删除按钮，可自己清空页面对话。
 6. 添加截图保存按钮，可点击将对话数据保存为图片。
 7. 加入语法高亮功能，同时markdown代码块实时转html标签。
 8. 代码块添加一键复制功能。
 9. 上下文对话状态下为节约 `tokens` ，当对话超过4轮后，则选取最新3轮作为上下文发送。为避免有人不点击删除按钮而导致页面积累大量对话，跟 `New Bing` 一样，当上下文对话超过20轮，则无法继续发送，会提示点击删除按钮清空页面数据！
 10. 美化页面，优化页面布局使得不同设备更好的自适应。

### 23 年 5.24 日更新

 1. 修复截图宽度很宽的问题。
 2. 添加 `GPT-4` 模型，需要有 `gpt-4` 权限的 `api key`。
 3. 添加停止响应按钮，输出结果不满意可停止响应。
 
### 24 年 5.30 日更新

 1. 添加代理url,api key环境变量输入方式。
 2. 适配部分中转接口输出错误信息提示。

## 交流与赞助

### 全栈学习交流1群：[799160455](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=jj15fOLBvm5U97kuj-Jgvvld2eDACl2o&authKey=fcll1nLa0V9wFMPkJGurdv%2FX%2FHlasFVHpS9vmtuFLofiqBD%2Fgl5fcjXBmg4E3Ovc&noverify=0&group_code=799160455) （已满员）

### 全栈学习交流2群：[879763865](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=mVTtPhPE_-BUOEbNu_IuO-4FZoMR6m43&authKey=heN7%2BG%2FFLoPj1tZ%2Blg%2FWS11WrzYkHkMTVgv9qg9aPGlR5pbEOmzvTBv7npYU1d56&noverify=0&group_code=879763865) 

<table>
    <tr>
        <td align="center"><img src="./项目示例图/微信.png" width="300"></td>
        <td align="center"><img src="./项目示例图/赞赏码.png" width="300"></td>
    </tr>
    <tr>
        <td align="center">联系我</td>
        <td align="center">支持本项目</td>
    </tr>
</table>
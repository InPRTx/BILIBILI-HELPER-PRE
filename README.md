<div align="center">
<h1 align="center">
BILIBILI-HELPER
</h1>

[![GitHub stars](https://img.shields.io/github/stars/JunzhouLiu/BILIBILI-HELPER-PRE?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/JunzhouLiu/BILIBILI-HELPER-PRE?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/network)
[![GitHub issues](https://img.shields.io/github/issues/JunzhouLiu/BILIBILI-HELPER-PRE?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/issues)
[![GitHub license](https://img.shields.io/github/license/JunzhouLiu/BILIBILI-HELPER-PRE?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/blob/main/LICENSE)
[![GitHub All Releases](https://img.shields.io/github/downloads/JunzhouLiu/BILIBILI-HELPER-PRE/total?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/releases)
[![Docker Pulls](https://img.shields.io/docker/pulls/superng6/bilibili-helper?style=flat-square)](https://hub.docker.com/r/superng6/bilibili-helper)
[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/JunzhouLiu/BILIBILI-HELPER-PRE?style=flat-square)](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/releases)
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FJunzhouLiu%2FBILIBILI-HELPER-PRE&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FJunzhouLiu%2FBILIBILI-HELPER.svg?type=flat-square)](https://app.fossa.com/projects/git%2Bgithub.com%2FJunzhouLiu%2FBILIBILI-HELPER?ref=badge_shield)

</div>

## 工具简介

这是一个利用 Linux Crontab ,云函数， Docker 等方式实现哔哩哔哩（Bilibili）每日任务投币，点赞，分享视频，直播签到，银瓜子兑换硬币，漫画每日签到，简单配置即可每日轻松获取 65 经验值，快来和我一起成为 Lv6
吧\~\~\~\~

**如果觉得好用，顺手点个 Star 吧 ❤**

**仓库地址：[JunzhouLiu/BILIBILI-HELPER](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE)**

**B 站赛事预测助手已发布，每天自动参与 KPL，LPL 赛事预测，赚取硬币。**

**仓库地址：[JunzhouLiu/bilibili-match-prediction](https://github.com/JunzhouLiu/bilibili-match-prediction)**

**请不要滥用相关 API，让我们一起爱护 B 站 ❤**


<div align="center">

[也可点击此处一键加群](https://qm.qq.com/cgi-bin/qm/qr?k=m_M1Fydi3MvrVAEM0Sp6hDfZF4N2SpXU&jump_from=webapi)

qq 群二维码

![qq群二维码](docs/IMG/qqgroup.png)

</div>

## 功能列表

- [x] 通过docker或者云函数执行定时任务。_【运行时间可自定义】_
- [x] 哔哩哔哩漫画每日自动签到，自动阅读 1 章节 。
- [x] 每日自动从热门视频中随机观看 1 个视频，分享一个视频。
- [x] 每日从热门视频中选取 5 个进行智能投币 _【如果投币不能获得经验了，则不会投币】_
- [x] 投币支持下次一定啦，可自定义每日投币数量。_【如果检测到你已经投过币了，则不会投币】_
- [x] 大会员月底使用快到期的 B 币券，给自己充电，一点也不会浪费哦，默认开启。_【已支持给指定 UP 充电】_
- [x] 大会员月初 1 号自动领取每月 5 张 B 币券和福利。
- [x] 每日哔哩哔哩直播自动签到，领取签到奖励。_【直播你可以不看，但是奖励咱们一定要领】_
- [x] Linux 用户支持自定义配置了。
- [x] 投币策略更新可配置投币喜好。_【可配置优先给关注的 up 投币】_
- [x] 自动送出即将过期的礼物。 _【默认开启，未更新到新版本的用户默认关闭】_
- [x] 支持推送执行结果到微信，钉钉，飞书等。

[点击快速开始使用](#使用说明)

[点击快速查看自定义功能配置](#自定义功能配置)

# 目录

- [目录](#目录)
  - [使用说明](#使用说明)
    - [获取运行所需的 Cookies](#获取运行所需的-cookies)
    - [一、使用 腾讯云函数](#一使用-腾讯云函数)
    - [二、使用 Docker](#二使用-docker)
    - [三、使用 Linux Crontab 方式](#三使用-linux-crontab-方式)
      - [使用bash](#使用bash)
      - [使用 `java -jar `](#使用-java--jar-)
    - [自定义功能配置](#自定义功能配置)
  - [订阅执行结果](#订阅执行结果)
    - [Server 酱 Turbo 版](#server-酱-turbo-版)
    - [Telegram 订阅执行结果](#telegram-订阅执行结果)
    - [企业微信](#企业微信)
    - [钉钉机器人](#钉钉机器人)
    - [PushPlus(Push+)](#pushpluspush)
  - [免责声明](#免责声明)
  - [API 参考列表](#api-参考列表)
  - [基于本项目的衍生项目](#基于本项目的衍生项目)
  - [致谢](#致谢)
  - [License](#license)
  - [Stargazers over time](#stargazers-over-time)

## 使用说明

### 获取运行所需的 Cookies

1. **Fork 本项目**
2. **获取 Bilibili Cookies**
3. 浏览器打开并登录 [bilibili 网站]()
4. 按 F12 打开 「开发者工具」 找到 应用程序/Application -\> 存储 -\> Cookies
5. 找到 `bili_jct` `SESSDATA` `DEDEUSERID` 三项，并复制值，后面需要用到。

![图示](docs/IMG/20201012001307.png)

### 一、使用 腾讯云函数

请参考[腾讯云函数部署](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/blob/main/docs/scf.md)

### 二、使用 Docker

请自行参阅 [基于本项目的衍生项目](#基于本项目的衍生项目)。

- **基于本项目的 docker 封装项目：[SuperNG6/docker-bilibili-helper](https://github.com/SuperNG6/docker-bilibili-helper)**

- **基于本项目的 docker 镜像：[superng6/bilibili-helper](https://hub.docker.com/r/superng6/bilibili-helper)**

### 三、使用 Linux Crontab 方式


#### 使用bash

1. 点击 [BILIBILI-HELPER/release][30]，下载已发布的版本，解压后将 jar 包手动上传到 Linux 服务器，使用 crontab 完成定时执行，如果使用`crontab`
   请记得`source /etc/profile`和`source ~/.bashrc`,建议直接使用仓库提供的[`start.sh`][31]脚本,注意修改脚本的 jar 包路径和 cookies 参数。

[30]: https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/releases/latest

[31]: https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/blob/main/start.sh

**crontab 命令示例**

`30 10 * * * sh /home/start.sh`

| args              | 说明               |
| ----------------- | ------------------ |
| 30 10 \* \* \*    | `crontab` 定时时间 |
| sh /home/start.sh | `start.sh`的路径   |

```bash
#!/bin/bash
source /etc/profile
source ~/.bashrc
source ~/.zshrc #其他终端请自行引入环境变量
echo $PATH
java -jar /home/BILIBILI-HELPER.jar DEDEUSERID SESSDATA BILI_JCT SCKEY >> /var/log/bilibili-help.log
# 注意将jar包路径替换为实际路径。将参数修改该你自己的参数，cookies中含有% * 等特殊字符需要转义。
```

#### 使用 `java -jar `

**jar命令参数列表**

参数顺序指的是`java -jar /home/BILIBILI-HELP.jar `命令后所跟的参数列表顺序。

| 参数顺序 | 参数          | 说明｜                                      |
| -------- | ------------- | ------------------------------------------- |
| 1        | DEDEUSERID    | 哔哩哔哩Cookies                             |
| 2        | SESSDATA      | 哔哩哔哩Cookies                             |
| 3        | BILI_JCT      | 哔哩哔哩Cookies                             |
| 4        | 推送渠道的Key | 单个参数的推送渠道，程序自动判断是哪个渠道，比如钉钉，企业微信，server酱    |
| 5        | 推送渠道的ID之类的 | 某些渠道的推送除了key还有id，id请跟在第五位（例如tg） |

**crontab任务示例：**

```bash
# *如果Cookies参数中包含特殊字符，例如`%`请使用`\`转义*,如果不执行可在命令前增加 source /etc/profile
# m h  dom mon dow   command
30 10 * * * java -jar /home/BILIBILI-HELP.jar DEDEUSERID SESSDATA BILI_JCT >/var/log/cron.log &
```

### 自定义功能配置

配置文件示例：

```json
{
  "matchGame": false,
  "showHandModel": false,
  "predictNumberOfCoins": 1,
  "minimumNumberOfCoins": 1000,
  "taskIntervalTime": 20,
  "numberOfCoins": 5,
  "reserveCoins": 10,
  "selectLike": 0,
  "monthEndAutoCharge": true,
  "giveGift": true,
  "upLive": "0",
  "chargeForLove": "14602398",
  "chargeDay": 28,
  "devicePlatform": "ios",
  "coinAddPriority": 1,
  "skipDailyTask": false,
  "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36 Edg/91.0.864.54"
}
```

**如果不知道自己的UA之类数据，以及看不懂每个值的含义，可以采用配置生成网页生成自己的配置，注意jar方式和docker方式运行无需填写cookies相关信息**

**[点击进入配置自动生成页面](https://utils.misec.top/index)**

**Windows/Linux 用户使用 jar 包时，`release`包中会包含一份`config.json`配置文件，只需将其和`BILIBILI-HELP.jar`放在同一目录即可，执行时优先加载外部配置文件**

配置文件参数示意

| Key                  | Value                | 说明                                                                   |
| -------------------- | -------------------- | ---------------------------------------------------------------------- |
| matchGame            | [false,true]         | 是否开启赛事预测。                                                     |
| showHandModel        | [false,true]         | true ：压赔率高的，false：压赔率低的                                   |
| predictNumberOfCoins | 1-10                 | 单次预测的硬币数量,默认为1                                             |
| minimumNumberOfCoins | [1,无穷大]           | 预留的硬币数，低于此数量不执行赛事预测。                               |
| taskIntervalTime     | [1,无穷大]           | 任务之间的执行间隔,默认10秒,云函数用户不建议调整的太长，注意免费时长。 |
| numberOfCoins        | [0,5]                | 每日投币数量,默认 5 ,为 0 时则不投币                                   |
| reserveCoins         | [0,4000]             | 预留的硬币数，当硬币余额小于这个值时，不会进行投币任务，默认值为 50    |
| selectLike           | [0,1]                | 投币时是否点赞，默认 0, 0：否 1：是                                    |
| monthEndAutoCharge   | [false,true]         | 年度大会员月底是否用 B 币券自动充电，默认 `true`。                     |
| giveGift             | [false,true]         | 直播送出即将过期的礼物，默认开启，如需关闭请改为 false                 |
| upLive               | [0,送礼 up 主的 uid] | 直播送出即将过期的礼物，指定 up 主，为 0 时则随随机选取一个 up 主      |
| chargeForLove        | [充电对象的 uid]     | 给指定 up 主充电，值为充电对象的 uid ,默认为14602398                   |
| chargeDay            | [1，28]              | 默认为每月28号                                                         |
| devicePlatform       | [ios,android]        | 手机端漫画签到时的平台，建议选择你设备的平台 ，默认 `ios`              |
| coinAddPriority      | [0,1]                | 0：优先给热榜视频投币，1：优先给关注的 up 投币                         |
| userAgent            | 浏览器 UA            | 用户可根据部署平台配置，可根据 userAgent 参数列表自由选取              |
| skipDailyTask        | [false,true]         | 是否跳过每日任务，默认`true`,如果关闭跳过每日任务，请改为`false`       |

- **tips:从1.0.0版本开始，随机视频投币有一定的概率会将硬币投给本项目的开发者。**
- **默认配置文件是给开发者充电，给自己充电或者给其他up充电，请改为对应的uid**
- **userAgent建议使用你自己真实常用浏览器UA，如果不知道自己的UA请到[配置生成页面查看你的UA](https://utils.misec.top/index)**

_ps：如果尝试给关注的 up 投币十次后（保不准你关注的是年更 up 主），还没完成每日投币任务，则切换成热榜模式，给热榜视频投币_

_投币数量代码做了处理，如果本日投币不能获得经验了，则不会投币，每天只投能获得经验的硬币。假设你设置每日投币 3 个，早上 7 点你自己投了 2 个硬币，则十点半时，程序只会投 1 个）_

## 订阅执行结果

### Server 酱 Turbo 版

目前 Turbo 版本的消息通道支持以下渠道

- 企业微信应用消息
- Android，
- Bark iOS，
- 企业微信群机器人
- 钉钉群机器人
- 飞书群机器人
- 自定义微信测试号
- 方糖服务号

1. 前往 [sct.ftqq.com](https://sct.ftqq.com/sendkey)点击登入，创建账号。
2. 点击点[SendKey](https://sct.ftqq.com/sendkey) ，生成一个 Key 变量名为 `SERVERPUSHKEY`，放在执行命令的第四位。
3. [配置消息通道](https://sct.ftqq.com/forward) ，选择方糖服务号，保存即可。
4. 推送效果展示
   ![图示](docs/IMG/wechatMsgPush.png)

**旧版推送渠道[sc.ftqq.com](http://sc.ftqq.com/9.version0) 即将与 4
月底下线，请前往[sct.ftqq.com](https://sct.ftqq.com/sendkey)生成`Turbo`版本的`Key`，注意，申请 Turbo 版 Key
后请配置消息通道，如果想沿用以前的推送方式，选择方糖服务号即可**

### Telegram 订阅执行结果

1. 在 Telegram 中添加 BotFather 这个账号，然后依次发送/start /newbot 按照提示即可创建一个新的机器人。记下来给你生成的 token。

2. 搜索刚刚创建的机器人的名字，并给它发送一条消息。

_特别注意：需要先与机器人之间创建会话，机器人才能下发消息，否则机器人无法主动发送消息，切记！_

3. 在 Telegram 中搜索 userinfobot，并给它发送一条消息，它会返回给你 chatid。

4. 将Telegram Token放在执行命令参数的第四位，chatid放在执行参数的第五位。

**执行示例**

```bash
# *如果Cookies参数中包含特殊字符，例如请使用`\`转义*,
java -jar /home/BILIBILI-HELP.jar DEDEUSERID SESSDATA BILI_JCT Telegram_Token chatid
```

### 企业微信

将企业微信的key放在执行参数的第四位。

### 钉钉机器人

1. 首先你得有个钉钉企业 [快速注册](https://oa.dingtalk.com/register.html)

2. [进入钉钉开放平台添加机器人](https://open-dev.dingtalk.com/#/corprobot)

3. 添加自定义关键词：BILIBILI

4. 将机器人的 Webhook 放在执行参数的第四位。


**执行示例**

```bash
# *如果Cookies参数中包含特殊字符，例如请使用`\`转义*,
java -jar /home/BILIBILI-HELP.jar DEDEUSERID SESSDATA BILI_JCT `https://oapi.dingtalk.com/robot/send?access_token=XXX`
```

### PushPlus(Push+)

1. [前往 PushPlus 获取 Token](https://www.pushplus.plus/push1.html)

2. 将获取到的 Token 放在执行命令的第四位。



## 免责声明

1. 本工具不会记录你的任何敏感信息，也不会上传到任何服务器上。（例如用户的 cookies 数据，cookies 数据均存在用户自己的设备上）
2. 本工具不会记录任何执行过程中来自 b 站的数据信息，也不会上传到任何服务器上。（例如 av 号，bv 号，用户 uid 等）。
3. 请不要把自己的敏感信息（账号，cookies等）提供给他人。（**网络安全教育普及任重而道远**）
4. 本工具源码仅在[JunzhouLiu/BILIBILI-HELPER-PRE](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE)开源。
5. 开源的目的单纯是技术分享，所有代码细节都公开。
6. 本项目不会增加类似于自动转发抽奖，秒杀，下载版权受限视频等侵犯 UP 主/B 站权益的功能。
7. 本项目遵守[MIT License](https://github.com/JunzhouLiu/BILIBILI-HELPER-PRE/blob/main/LICENSE)，因使用造成的任何损失，纠纷等，和开发者无关，请各位知悉。

## API 参考列表

- [SocialSisterYi/bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect)
- [happy888888/BiliExp](https://github.com/happy888888/BiliExp)

## 基于本项目的衍生项目

- **基于本项目的 docker 封装项目：[SuperNG6/docker-bilibili-helper](https://github.com/SuperNG6/docker-bilibili-helper)**

- **基于本项目的 docker 镜像：[superng6/bilibili-helper](https://hub.docker.com/r/superng6/bilibili-helper)**

- **基于本项目的 k8s 项目：[yangyang0507/k8s-bilibili-helper](https://github.com/yangyang0507/k8s-bilibili-helper)**

## 致谢

感谢 JetBrains 对本项目的支持。

[![JetBrains](docs/IMG/jetbrains.svg)](https://www.jetbrains.com/?from=BILIBILI-HELPER)

## License

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FJunzhouLiu%2FBILIBILI-HELPER.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FJunzhouLiu%2FBILIBILI-HELPER?ref=badge_large)

## Stargazers over time

[![Stargazers over time](https://starchart.cc/JunzhouLiu/BILIBILI-HELPER.svg)](https://starchart.cc/JunzhouLiu/BILIBILI-HELPER)

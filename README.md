##  悟空IM（让信息传递更简单）

高性能通用通讯服务，支持即时通讯，消息推送，物联网通讯，音视频信令，直播弹幕，客服系统，AI通讯，即时社区等场景。

[English](./README_EN.md)

<p align="center">
<img align="left" width="200" src="./docs/logo.png">
<ul>
<li><strong>QQ群</strong>: <a href="#">750224611</a></li>
<li><strong>微信</strong>: <a href="#">wukongimgo（备注进群）</a></li>
<li><strong>官网</strong>: https://githubim.com</li>
<li><strong>通讯协议</strong>: <a href="./docs/protocol.md">WuKongIM协议</a></li>
<li><strong>提问</strong>: https://github.com/WuKongIM/WuKongIM/issues</li>
<li><strong>文档</strong>: http://www.githubim.com/docs</li>
</ul>
</p>

[![](https://img.shields.io/github/license/WuKongIM/WuKongIM?color=yellow&style=flat-square)](./LICENSE)
[![](https://img.shields.io/badge/go-%3E%3D1.17-30dff3?style=flat-square&logo=go)](https://github.com/WuKongIM/WuKongIM)
[![](https://img.shields.io/badge/go%20report-A+-brightgreen.svg?style=flat)](https://goreportcard.com/report/github.com/WuKongIM/WuKongIM)

## 特点

* 没有依赖任何第三方组件，部署简单，一条命令即可启动
* 自研消息数据库，消息分区永久存储
* 自研二进制协议，支持自定义协议
* 消息通道和消息内容全程加密，防中间人攻击和串改消息内容。
* 支持一个账号多设备登录，数据实时同步
* 简单易用，性能强劲，MAC笔记本单机测试16w多/秒的消息(包含存储)吞吐量，为了达到这性能和简单易用，完全自主实现消息存储，无如何第三方组件依赖，一条命令即可启动服务
* 扩展性强 采用频道设计理念，目前支持群组频道，点对点频道，后续可以根据自己业务自定义频道可实现机器人频道，客服频道等等功能。
* 同时无差别支持tcp，websocket。
* 频道支持万人订阅者。


## 适用场景

#### 即时通讯

* 群频道支持
* 个人频道支持
* 消息永久存储
* 离线消息推送支持
* 最近会话维护

#### 消息推送/站内消息

* 群频道支持
* 个人频道支持
* 离线消息推送支持

#### 物联网通讯

* mqtt协议支持（待开发）
* 支持发布与订阅

#### 音视频信令服务器

* 支持临时指令消息投递

#### 直播弹幕

* 临时消息投递

* 临时订阅者支持

#### 客服系统

* 客服频道支持

* 消息支持投递给第三方服务器

* 第三方服务器可决定分配指定的订阅者成组投递

#### 实时AI反馈

* 支持客户端发的消息推送给第三方服务器，第三方服务器反馈给AI后返回的结果再推送给客户端

#### 即时社区

* 社区频道支持
* 支持topic模式的消息投递


## 快速启动

```go 

go run main.go

```

## 客户端SDK

[Android SDK](https://github.com/WuKongIM/WuKongIMAndroidSDK.git)

[iOS SDK](https://github.com/WuKongIM/WuKongIMiOSSDK.git)

[JS SDK](https://github.com/WuKongIM/WuKongIMJSSDK.git)

[Flutter SDK](https://github.com/WuKongIM/WuKongIMFlutterSDK.git)

SDK的使用请查看[文档](http://www.githubim.com/docs)

## 通过Docker Compose运行

```
$ docker-compose up -d
```

## 架构

WuKongIM 没有依赖任何第三方组件

***完整架构***

<img src="./docs/architecture/architecture.png" alt="Architecture"/>

***认证逻辑***

<img src="./docs/architecture/auth.png" alt="Architecture"/>

***消息处理逻辑***

<img src="./docs/architecture/processmsg.png" alt="Architecture"/>


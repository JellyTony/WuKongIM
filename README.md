## WuKongIM (Make information transfer easier)

WuKongIM is a high-performance universal communication service that supports various scenarios such as instant messaging, message push, IoT communication, audio and video signaling, live broadcasting with bullet comments, customer service systems, AI communication, and instant communities.

(Note: This project is a general underlying instant messaging service. The upper layer needs to dock with its own specific business system (which can be easily docked with its own business system through the webhook and datasource mechanism). The core of this project mainly maintains a large number of long connections of clients and delivers messages according to the message rules of third-party business systems.)

`This project needs to be compiled in a go1.20.0 or higher version.`

[中文文档](./README_CN.md)

<p align="center">
<img align="left" height="110" src="./docs/logo.png">
<ul>
<!-- <li><strong>QQ group</strong>: <a href="#">496193831</a></li> -->
<li><strong>Website</strong>: http://www.githubim.com</li>
<li><strong>Protocol</strong>: <a href="https://githubim.com/guide/proto">WuKongIM Protocol</a></li>
<li><strong>Issues</strong>: https://github.com/WuKongIM/WuKongIM/issues</li>
<li><strong>Docs</strong>: http://www.githubim.com</li>
</ul>
</p>

[![](https://img.shields.io/github/license/WuKongIM/WuKongIM?color=yellow&style=flat-square)](./LICENSE)
[![](https://img.shields.io/badge/go-%3E%3D1.20-30dff3?style=flat-square&logo=go)](https://github.com/WuKongIM/WuKongIM)
[![](https://img.shields.io/badge/go%20report-A+-brightgreen.svg?style=flat)](https://goreportcard.com/report/github.com/WuKongIM/WuKongIM)

Features
--------

- 📚 Fully self-developed: WuKongIM uses a self-developed message database, binary protocol, and network library, and supports custom protocols.
- 🚀 High performance: WuKongIM can handle millions of online users and has a throughput of 160,000 messages per second (including database operations).
- 🔔 Zero dependencies: WuKongIM has no third-party dependencies and is easy to deploy.
- 🔐 Security: WuKongIM encrypts both message channels and message content to prevent man-in-the-middle attacks and message tampering.
- 🧱 Highly extensible: WuKongIM uses a channel-based design and currently supports group and point-to-point channels. It can be extended to support custom channels for use cases such as chatbots and customer service.

TODO
---------------

- [x] Supports custom messages
- [x] Supports subscription/publisher mode
- [x] Supports personal/group chat/customer service/community news channels
- [x] Supports channel blacklists
- [x] Supports channel whitelists
- [x] Supports permanent message storage, device switching, and message retention
- [x] Supports online status and multiple devices logged in simultaneously with the same account
- [x] Supports real-time synchronization of messages across multiple devices
- [x] Supports server-side maintenance of user's recent conversation list
- [x] Supports command messages
- [x] Supports offline command interface
- [x] Supports Webhook, easy integration with your own business system
- [x] Supports Datasoure, seamless integration with your own business system data source
- [x] Supports WebSocket connections
- [x] Supports TLS 1.3
- [x] Development of monitoring system
- [ ] Support for Windows system deployment


Quick Start
---------------

```
docker run -d -p 5001:5001 -p 5100:5100 -p 5200:5200 -p 5300:5300 -e WK_EXTERNAL_IP=xxx.xxx.xxx.xx --name wukongim -v ~/wukongim:/root/wukongim wukongim/wukongim:latest
```

`WK_EXTERNAL_IP: The external IP address of the server used for client connections. If testing only and the client and server are on the same LAN, the LAN IP address of the deployed server can be used here.`

View System information: http://127.0.0.1:5001/varz

View Monitor information: http://127.0.0.1:5300/web

Demo: http://imdemo.githubim.com

For more deployment options, see the [documentation](http://githubim.com/guide/quickstart).


SDK source code and demos
---------------

[iOS Demo and SDK Source Code](https://github.com/WuKongIM/WuKongIMiOSSDK)

[Android Demo and SDK Source Code](https://github.com/WuKongIM/WuKongIMAndroidSDK)

[Web Demo and SDK Source Code](https://github.com/WuKongIM/WuKongIMJSSDK)

[Uniapp Demo and SDK Source Code](https://github.com/WuKongIM/WuKongIMUniappSDK)

[Flutter Demo and SDK Source Code (to be improved)](https://github.com/WuKongIM/WuKongIMFlutterSDK)

Applicable Scenarios
---------------

#### Instant Messaging

* Supports group channels
* Supports personal channels
* Supports permanent message storage
* Supports offline message push
* Supports recent conversation maintenance

#### Message Push/Site Message

* Supports group channels
* Supports personal channels
* Supports offline message push

#### IoT Communication

* Supports MQTT protocol (to be developed)
* Supports publish and subscribe

#### Audio and Video Signaling Server

* Supports temporary command message delivery

#### Live Broadcast Bullet Screens

* Supports temporary message delivery
* Supports temporary subscriber support

#### Customer Service System

* Supports customer service channels
* Messages can be delivered to third-party servers
* Third-party servers can decide to allocate designated subscribers to deliver messages in groups

#### Real-time AI Feedback

* Supports pushing messages sent by clients to third-party servers, and the results returned by AI after being fed back by third-party servers are pushed back to clients

#### Instant Community

* Supports community channels
* Supports message delivery in topic mode


Monitor
---------------

![image](./docs/screen1.png)
![image](./docs/screen2.png)
![image](./docs/screen3.png)
![image](./docs/screen4.png)
![image](./docs/screen5.png)

Wechat
---------------

If necessary, add me and I will invite you to the group. My WeChat ID is wukongimgo.

![image](./wechat.jpg)


License
---------------

WuKongIM is licensed under the [Apache License 2.0](./LICENSE).
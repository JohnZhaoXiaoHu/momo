### 直播源码,短视频,直播带货,游戏陪玩,仿比心,猎游,tt语音聊天,美女约玩,陪玩系统源码开黑,约玩源码

----------------
<div align=center>
<img src="https://img.shields.io/badge/php-7.3-blue"/>
<img src="https://img.shields.io/badge/golang-1.13-blue"/>
<img src="https://img.shields.io/badge/gin-1.4.0-lightBlue"/>
<img src="https://img.shields.io/badge/vue-2.6.10-brightgreen"/>
<img src="https://img.shields.io/badge/element--ui-2.12.0-green"/>
<img src="https://img.shields.io/badge/gorm-1.9.12-red"/>
</div>

[English](./README-en.md) | 简体中文

### 前端: VUE 移动端: Android + ios

### 微服务（Docker容器）组成：

- **goim** ：不多说 B站 IM架构
- **livego** ：基于golang开发的高性能rtmp服务器 实测机型：阿里云32核64G独享服务器 30000路并发拉流，cpu占用率不到50%！
- **webrtc** ：Janus Gateway：Meetecho优秀的通用WebRTC服务器（SFU）；
- **MongoDB** ：云时代构建的基于文档的分布式数据库；
- **Redis**：内存中的数据结构存储，用作数据库，缓存和消息代理；
- **kafka** ：队列 群聊，私聊，消息通知等。
- **Coturn** ：TURN和STUN Server的开源项目；
- **Nginx** ：高性能负载平衡器，Web服务器和有HTTP3 / Quiche和Brtoli支持的反向代理；
- **Docker**：用于构建、部署和管理容器化应用程序的平台。
- **后台管理界面**: php（老业务php后台）+ gin（API接口重构）+ vue + Element-UI 
----------------


**技术群：**
![](https://img-blog.csdnimg.cn/20200623093238797.png)


纯技术群，入群有一定门槛，谢谢理解。
----------------
微信：BCFind5 【请备注好信息】

博客地址：https://blog.csdn.net/u012115197/article/details/106916635

Gitee：https://gitee.com/baoyalive/baoyalive.git


----------------

### 商业合作 （UI设计，定制开发，系统重构，代理推广等）

| 类目        | 价格   |  商业授权  |
| --------   | -----:  | :----:  |
| 基础开源版本（php+go的基础版本仅供学习使用）      | ￥0        |   无（不可商用）     |
| php国内商用版本       |   ￥15000  |   有（可以商用）  |
| golang海外商用版本		|    ￥30000起|  有（可以商用）|

----------------

[后台演示地址：](http://www.jinqianlive.com/admin) http://www.jinqianlive.com/admin

账号 ：test
密码： test

----------------
[直播短视频app下载](https://baoya.lanzous.com/imcL9e57tej) https://baoya.lanzous.com/imcL9e57tej（用手机浏览器打开下载，不要用微信直接下载）

----------------
[陪玩app下载](http://app.6sjs.com/wej8) http://app.6sjs.com/wej8  （用手机浏览器打开下载，不要用微信直接下载）
  
----------------
IOS 视频演示：https://pan.baidu.com/s/18KaHu-39TMQLetb0m7XD0Q 提取码：v929

----------------

文档地址：http://www.jinqianlive.com/appapi/listAllApis.php?type=expand

----------------

**前端展示**
![前端展示](https://img-blog.csdnimg.cn/20200908194734911.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)

**后台界面**
![后台界面](https://img-blog.csdnimg.cn/20200907180807339.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)


----------------

### 入门推荐书籍

* [FFmpeg从入门到精通](https://book.douban.com/subject/30178432/) - 强烈推荐
* [直播系统开发：基于Nginx与Nginx-rtmp-module](https://book.douban.com/subject/30423374/)
* [WebRTC权威指南](https://book.douban.com/subject/26915289/)
* [CDN技术详解](https://book.douban.com/subject/10759173/)

### 技术结构
## 前端 
- **集小视频/IM聊天/直播等功能于一体的直播项目。界面仿制抖音|火山小视频|陌陌直播|比心陪玩等。**

#### *注意：*前端的具体细技术细节请移至前端篇赘述，本贴暂不描述前端内容。
![陪玩app](https://img-blog.csdnimg.cn/20210406163759968.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)

## 后端

**系统开发语言**
-  **PHP|golang 视频互动系统由 WEB 系统、REDIS 服务、MYSQL 服务、视频服务、聊天服务、后台管理系统和定时监控组成，后台管理采用PHP + golang 语言开发，所有服务提供横向扩展。**

1. WEB 系统提供页面、接口逻辑。
2. REDIS 服务提供数据的缓存、存储动态数据。
3. MYSQL 服务提供静态数据的存储。
4. 视频服务提供视频直播，傍路直播，转码、存储、点播等 支持腾讯云 阿里云 七牛等 自建流媒体服务器等（包括两套成熟方案 nginx_rtmp 和 golang的）。
5. golang +kafka 队列 聊天服务提供直播群聊，私聊，消息通知等。
6. consul + grpc 系统监控：监听主播异常掉线情况、直播消息推送等。
 
------------
## 分布式架构

	注：本教程适用于 Go 1.13 版本，因为 Go 1.11 才正式引入了 Go Module 作为包管理器。

**针对市面上现有的直播系统多为单机裸奔版本，系统臃肿，业务耦合 IM API等不可横向扩展，所以采用分布式尤为必要，采用到技术如下：**

后台管理：**laravel** 

分布式：**go mirco + micro api + etcd + kafka**等 

前端：**vue**

移动端： **ios+android+小程序**等

数据库：**mysql+redis**

通讯框架：**gprc**

长连接通讯协议：**protocol buffers**


### 环境搭建
  **准备工具先，比如需要开发的东西，虚拟机镜像，工具等等。**

网盘链接：https://pan.baidu.com/s/1WsfqcAZ8Ph6id39gbOMjbQ 
提取码：7nq3
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922185921775.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)

**安装虚拟机**
> 1.安装虚拟机 centos7 系统  镜像链接: [https://www.centos.org/download/](https://www.centos.org/download/)	此处省略··

**安装golang** 
```bash
wget http://www.golangtc.com/static/go/go1.3.linux-amd64.tar.gz
```
```bash
tar -C /usr/local -zxvf  go1.3.linux-amd64.tar.gz 
```

```bash
vim /etc/profile	
// 在最后添加
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
export GOPATH="$HOME/go
export GO111MODULE=on
export GOPROXY=https://goproxy.io
```
**成功**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922210610471.png#pic_center)

**安装etcd**
```bash
curl -L https://github.com/coreos/etcd/releases/download/v3.3.2/etcd-v3.3.2-linux-amd64.tar.gz -o etcd-v3.3.2-linux-amd64.tar.gz
```
```bash
tar -zxf etcd-v3.3.2-linux-amd64.tar.gz
```
```bash
解压后是一些文档和两个二进制文件etcd和etcdctl。etcd是server端，etcdctl是客户端。
```
```bash
mv etcd-v3.3.2-linux-amd64/etcd* /$GOPATH/bin
```
```bash
./etcd 
```
**成功**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922213137699.png#pic_center)

**安装 Protobuf 相关工具**

```bash
先创建项目文件 mkdir /www/go/live
```
```bash
cd /www/go/live
```
```bash
go mod init live
#自动生成go.mod文件
```
**Go Micro是Go开发微服务的RPC框架**
```bash
go get github.com/micro/go-micro
```
**安装 protoc**
```bash
可以从这里 https://github.com/protocolbuffers/protobuf/releases 下载`最新`版的 protoc 截止教程结束本人下载最新的是protobuf-all-3.13.0.tar：
./configure
make && make install
注意：没有c++ 的提前安一下，否则编译不过去，这种问题就不用赘述了，这个都不懂也没必要继续往下看了
```
```bash
protoc --version
```
![成功](https://img-blog.csdnimg.cn/20200922221355356.png#pic_center)

**安装 protoc-gen-micro**
```bash
go get -u github.com/micro/protoc-gen-micro
```
**安装 protoc-gen-go**
```bash
go get -u github.com/golang/protobuf/protoc-gen-go

cp protoc-gen-* /usr/local/bin/

至此你的$GOPATH/bin下有如下文件 复制一份到/usr/local/bin 下
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922222247686.png#pic_center)

**编写代码测试一把**
```golang
mkdir /www/go/live/proto
然后在 proto 目录下创建一个 Protobuf 格式的服务接口声明文件 live.proto：
```
```proto3
syntax = "proto3";

service Live {
rpc Call(LiveRequest) returns (LiveResponse) {}
}

message LiveRequest {
string name = 1; 
}

message liveResponse {
string result = 1;
}
```
```bash
protoc自动生成代码
protoc --proto_path=. --micro_out=. --go_out=. proto/live.proto
```
>此时proto文件下多出几个文件：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922224029282.png#pic_center)

**编写GO服务实现代码 live 目录下 创建 mian.go**
```golang
package main

import (
	"context"
	"fmt"
	"github.com/micro/go-micro"
	proto "live/proto"
)

type LiveServiceHandler struct{}

func (g *LiveServiceHandler)Call(ctx context.Context, req *proto.LiveRequest, rsp *proto.LiveResponse) error {
	rsp.Result = "我的github：https://github.com/DOUBLE-Baller/" + req.Name
	return nil
}

func main()  {
	// 创建新的服务
	service := micro.NewService(
		micro.Name("go.micro.api.Live"), //go.micro.api 命名空间
	)

	// 初始化，会解析命令行参数
	service.Init()

	// 注册处理器，调用 Live 服务接口处理请求
	proto.RegisterLiveHandler(service.Server(), new(LiveServiceHandler))

	// 启动服务
	if err := service.Run(); err != nil {
		fmt.Println(err)
	}
}
```
```golang
go run main.go
```
```bash
如图表示成功启动服务 注意：添加环境变量 MICRO_REGISTRY=etcd 来统一设置 或者使用go run main.go --registry=etcd 命令手动注册服务
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020092223034366.png#pic_center)
失败如下图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922225010494.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)
```bash
如遇此错误：添加go.mod最后一行即可！
replace google.golang.org/grpc => google.golang.org/grpc v1.26.0
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200923092941557.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)


**利用 go micro 提供 HTTP 服务接口**
```bash
go get github.com/micro/micro/v2

安装完成后，会在 $GOPATH/bin 目录下创建一个 micro 可执行文件，cp 到/user/local/bin 下即可
```
```bash
micro api --handler=rpc
```
```bash
如下表示启动成功 默认端口8080 
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922233014118.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)

访问IP:8080 如图 有防火墙的请添加规则放开8080端口即可访问！![在这里插入图片描述](https://img-blog.csdnimg.cn/20200922233410216.png#pic_center)

**ok 到此基础环境搭建完成 下面运行远程调用 api**
```bash
micro call go.micro.api.Live Live.Call '{"name": "momo"}'
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200923111240482.png#pic_center)


### 项目代码
>项目目录：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200923112617559.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)

> server:       服务启动入口 
>
> config:       服务配置
>
> app:     每个服务私有代码 
>
> comm:   服务共有代码 
>
> sql:          项目sql文件
>
> test:         长连接测试脚本


**app服务介绍**

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200923113249111.png#pic_center)

```bash
1.tcp_conn
维持与客户端的TCP长连接，心跳，以及TCP拆包粘包，消息编解码
2.ws_conn
维持与客户端的WebSocket长连接，心跳，消息编解码
3.logic
设备信息，好友信息，群组信息管理，消息转发逻辑
4.user
可以根据自己的业务需求，进行扩展,也可以替换成自己的业务服务器
```
**客户端接入流程**
```bash
1.调用LogicExt.RegisterDevice接口，完成设备注册，获取设备ID（device_id）,注意，一个设备只需完成一次注册即可，后续如果本地有device_id,就不需要注册了，举个例子，如果是APP第一次安装，就需要调用这个接口，后面即便是换账号登录，也不需要重新注册。
2.调用UserExt.SignIn接口，完成账户登录，获取账户登录的token。
3.建立长连接，使用步骤2拿到的token，完成长连接登录。
如果是web端,需要调用建立WebSocket时,将user_id,device_id,token，以URL参数的形式传递到服务器，完成长连接登录，例如：ws://localhost:8081/ws?user_id={user_id}&device_id={device_id}&token={token}
如果是APP端，就需要建立TCP长连接，在完成建立TCP长连接时，第一个包应该是长连接登录包（SignInInput），如果信息无误，客户端就会成功建立长连接。
4.使用长连接发送消息同步包（SyncInput），完成离线消息同步，注意：seq字段是客户端接收到消息的最大同步序列号，如果用户是换设备登录或者第一次登录，seq应该传0。
接下来，用户可以使用LogicExt.SendMessage接口来发送消息，消息接收方可以使用长连接接收到对应的消息。
```
```
未完待续
```


## 视频服务

**RTMP服务添加一个application这个名字可以任意起，也可以起多个名字，由于是直播我就叫做它live，如果打算弄多个序列的直播就可以live_cctv。**
   
    #user  nobody;
    worker_processes  1;
    
    #error_log  logs/error.log;
    #error_log  logs/error.log  notice;
    #error_log  logs/error.log  info;
    
    #pid        logs/nginx.pid;
    
    
    events {
        worker_connections  1024;
    }
    
    rtmp {  #RTMP server
        server {    
            listen 1935;  #server port
            chunk_size 4096;  #chunk_size
            # vod server
            application vod {
                play /mnt/hgfs/dn_class/vod; #media file position
            }
            # live server 1
        application live{ #Darren live first add
            live on;
        }
            # live server 2
        application live_cctv{ #Darren live  add
            live on;
        }
        }
    }
    ........
    其他配置不需理会

**在Ubuntu端用ffmpeg产生一个模拟直播源，向rtmp服务器推送**

**推流**

`ffmpeg -re -i /mnt/hgfs/dn_class/vod/35.mp4 -c copy -f flv rtmp://192.168.100.33/live/35` 


*注意，源文件必须是H.264+AAC编码的*


**拉流**

`ffplay rtmp://192.168.100.33/live/35`


**点播配置**

1. 建立媒体文件夹`/mnt/hgfs/dn_class/vod`
**把媒体文件 35.mp4复制到/mnt/hgfs/dn_class/vod目录下。
然后我们就可以开启一个视频点播的服务了。打开配置文件nginx.conf（路径/usr/local/nginx/conf/nginx.conf），添加RTMP的配置。**

```
    #user  nobody;
    worker_processes  1;
    
    #error_log  logs/error.log;
    #error_log  logs/error.log  notice;
    #error_log  logs/error.log  info;
    
    #pid        logs/nginx.pid;
    
    
    events {
        worker_connections  1024;
    }
    
    rtmp {  #RTMP server
        server {    
            listen 1935;  #server port
            chunk_size 4096;  #chunk_size
            application vod {
                play /mnt/hgfs/dn_class/vod; #media file position
            }
        }
    }
    ........
    其他配置不需理会
```			
------------

## goim聊天服务

#### 特性
 * 轻量级
 * 高性能
 * 纯Golang实现
 * 支持单个、多个、单房间以及广播消息推送
 * 支持单个Key多个订阅者（可限制订阅者最大人数）
 * 心跳支持（应用心跳和tcp、keepalive）
 * 支持安全验证（未授权用户不能订阅）
 * 多协议支持（websocket，tcp）
 * 可拓扑的架构（job、logic模块可动态无限扩展）
 * 基于Kafka做异步消息推送

## 安装
### 一、安装依赖
```sh
$ yum -y install java-1.7.0-openjdk
```

### 二、安装Kafka消息队列服务

kafka在官网已经描述的非常详细，在这里就不过多说明，安装、启动请查看[这里](http://kafka.apache.org/documentation.html#quickstart).

### 三、搭建golang环境
1.下载源码(根据自己的系统下载对应的[安装包](http://golang.org/dl/))
```sh
$ cd /data/programfiles
$ wget -c --no-check-certificate https://storage.googleapis.com/golang/go1.5.2.linux-amd64.tar.gz
$ tar -xvf go1.5.2.linux-amd64.tar.gz -C /usr/local
```
2.配置GO环境变量
(这里我加在/etc/profile.d/golang.sh)
```sh
$ vi /etc/profile.d/golang.sh
# 将以下环境变量添加到profile最后面
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
export GOPATH=/data/apps/go
$ source /etc/profile
```

### 四、部署im
1.下载goim及依赖包
```sh
$ yum install hg
$ go get -u github.com/Terry-Mao/goim
$ mv $GOPATH/src/github.com/Terry-Mao/goim $GOPATH/src/goim
$ cd $GOPATH/src/goim
$ go get ./...
```

2.安装router、logic、comet、job模块(配置文件请依据实际机器环境配置)
```sh
$ cd $GOPATH/src/goim/router
$ go install
$ cp router-example.conf $GOPATH/bin/router.conf
$ cp router-log.xml $GOPATH/bin/
$ cd ../logic/
$ go install
$ cp logic-example.conf $GOPATH/bin/logic.conf
$ cp logic-log.xml $GOPATH/bin/
$ cd ../comet/
$ go install
$ cp comet-example.conf $GOPATH/bin/comet.conf
$ cp comet-log.xml $GOPATH/bin/
$ cd ../logic/job/
$ go install
$ cp job-example.conf $GOPATH/bin/job.conf
$ cp job-log.xml $GOPATH/bin/
```
到此所有的环境都搭建完成！

### 五、启动im
```sh
$ cd /$GOPATH/bin
$ nohup $GOPATH/bin/router -c $GOPATH/bin/router.conf 2>&1 > /data/logs/goim/panic-router.log &
$ nohup $GOPATH/bin/logic -c $GOPATH/bin/logic.conf 2>&1 > /data/logs/goim/panic-logic.log &
$ nohup $GOPATH/bin/comet -c $GOPATH/bin/comet.conf 2>&1 > /data/logs/goim/panic-comet.log &
$ nohup $GOPATH/bin/job -c $GOPATH/bin/job.conf 2>&1 > /data/logs/goim/panic-job.log &
```
如果启动失败，默认配置可通过查看panic-xxx.log日志文件来排查各个模块问题.

### 六、测试
## Arch
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200908200113599.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTIxMTUxOTc=,size_16,color_FFFFFF,t_70#pic_center)


### Benchmark Server
| CPU | Memory | OS | Instance |
| :---- | :---- | :---- | :---- |
| Intel(R) Xeon(R) CPU E5-2630 v2 @ 2.60GHz  | DDR3 32GB | Debian GNU/Linux 8 | 1 |

### Benchmark Case
* Online: 1,000,000
* Duration: 15min
* Push Speed: 40/s (broadcast room)
* Push Message: {"test":1}
* Received calc mode: 1s per times, total 30 times

### Benchmark Resource
* CPU: 2000%~2300%
* Memory: 14GB
* GC Pause: 504ms
* Network: Incoming(450MBit/s), Outgoing(4.39GBit/s)

### Benchmark Result
* Received: 35,900,000/s

推送协议可查看[push http协议文档](./docs/push.md)

## 配置

TODO

## 例子

Websocket: [Websocket Client Demo](https://github.com/DOUBLE-Baller/WebRTC_IM/tree/master/im/examples/javascript)

Android: [Android](https://github.com/DOUBLE-Baller/WebRTC_IM/tree/master/goim-java-sdk)

iOS: [iOS](https://github.com/DOUBLE-Baller/WebRTC_IM/tree/master/goim-oc-sdk)

## 文档
[push http协议文档](./docs/push.md)推送接口

## 集群

### comet

comet 属于接入层，非常容易扩展，直接开启多个comet节点，修改配置文件中的base节点下的server.id修改成不同值（注意一定要保证不同的comet进程值唯一），前端接入可以使用LVS 或者 DNS来转发

### logic

logic 属于无状态的逻辑层，可以随意增加节点，使用nginx upstream来扩展http接口，内部rpc部分，可以使用LVS四层转发

### kafka

kafka 可以使用多broker，或者多partition来扩展队列

### router

router 属于有状态节点，logic可以使用一致性hash配置节点，增加多个router节点（目前还不支持动态扩容），提前预估好在线和压力情况

### job

job 根据kafka的partition来扩展多job工作方式，具体可以参考下kafka的partition负载

------------

==问题反馈==

**在使用中有任何问题，欢迎反馈给我们，可以用以下联系方式跟我们交流**

English | [简体中文](./README.md)



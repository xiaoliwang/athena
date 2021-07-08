# Go 语言笔记

## gRPC

health check



服务发现

服务提供者

服务消费者



register

poll

call 



外挂注册



平滑发布



平滑退出

kill provider

需要通知 Discovery 注销

heath check 标记失败

shutdown  两个心跳周期



服务发现--客户端发现

客户端使用一个负载均衡算法



服务发现--服务端发现

consul template + nginx

kubernets + etcd

ingress 



pod（app + lb）

service  mesh

sidecar



推荐 UNIX环境高级编程



cap 理论

zookeeper 保证 cp

Eureka 保证 ap

Nacos 推荐使用



注册时间延迟

注销事件延迟（health check 保障）



Eureka  原理

异步注册

上线 renew

下线 cancel

三个生命周期后，没有请求，设置过期

protect 机制

15 分钟心跳低于期望值 * 85%，开启自我保护，保留过期服务不删除。

发给 Eureka 一个节点，会复制给其他节点。

Eureka 挂掉，不要重启。



多集群

共用 db

独立缓存

订阅 binlog 针对所有 cache 做处理



推荐：Google SRE



多集群

Health Check 高达 30%。解决方法是子集算法。

https://xargin.com/limiting-conn-wih-subset/



多租户



Nginx upsync



go-kit （可玩性较大）

go-micro

go-zero



binlog 读取使用 canal

Mysql 并行复制
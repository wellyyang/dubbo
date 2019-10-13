### 项目学习

#### 项目结构

1. dubbo-common 公共逻辑模块：提供工具类和通用模型。
2. dubbo-remoting 远程通信模块：提供通用的客户端和服务端的通讯功能。
3. dubbo-rpc 远程调用模块：抽象各种协议，以及动态代理，只包含一对一的调用，不关心集群的管理。
4. dubbo-cluster 集群模块：将多个服务提供方伪装为一个提供方，包括：负载均衡, 集群容错，路由，分组聚合等。集群的地址列表可以是静态配置的，也可以是由注册中心下发。
5. dubbo-registry 注册中心模块：基于注册中心下发地址的集群方式，以及对各种注册中心的抽象。
6. dubbo-monitor 监控模块：统计服务调用次数，调用时间的，调用链跟踪的服务。
7. dubbo-config 配置模块：是 Dubbo 对外的 API，用户通过 Config 使用Dubbo，隐藏 Dubbo 所有细节。
8. dubbo-container 容器模块：是一个 Standlone 的容器，以简单的 Main 加载 Spring 启动，因为服务通常不需要 Tomcat/JBoss 等 Web 容器的特性，没必要用 Web 容器去加载服务。
9. dubbo-filter 过滤器模块：提供了内置的过滤器。
10. dubbo-plugin 插件模块：提供了内置的插件。
11. dubbo-demo 快速启动示例。
12. dubbo-test 测试模块。
13. bom
  * dubbo-dependencies-bom/pom.xml 统一定义了 Dubbo 依赖的三方库的版本号
  * dubbo-bom/pom.xml 统一定义了 Dubbo 的版本号
  * dubbo/pom.xml ，Dubbo Parent Pom
  * dubbo/all/pom.xml ，Dubbo All Pom ，定义了 Dubbo 的打包脚本
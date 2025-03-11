**Spring Cloud:**

1. 路由：就是将数据包从源节点传输到目标节点的过程

2. 网关：是在计算机网络中充当连接器和中转站的设备或系统（nginx）

3. 集群架构(增加多个服务器，网关进行协调负载均衡)可以解决大并发问题 有模块化升级和多语言团队的**问题**

4. 分布式架构：**一个大型应用被拆分成多个小应用分布部署在多个服务器** 是一种工作/架构模式

   集群：集群是一种物理形态（多个服务器）<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250304175535860.png" alt="image-20250304175535860" style="zoom: 67%;" />

    将不同的功能能代码块以及数据库，部署到多个服务器 **每一个模块就是一个微服务**

   <img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250304173955039.png" alt="image-20250304173955039" style="zoom: 67%;" />[SpringCloud-图例.svg](file:///D:/a网盘资料BaiduNetdiskDownload/Spring Cloud/资料(1)/SpringCloud-图例.svg)

5. RPC：一种跨进程通信协议，允许像调用本地方法一样调用远程服务远程过程调用 

   是一种通过网络从远程计算机程序上请求服务的技术 比如多个分布式架构下服务器之间的数据通信

6. 服务熔断机制：快速失败策略 ，防止服务雪崩

7. openfeign：Spring Cloud中的一个声明式的HTTP客户端，它使编写HTTP客户端变得更加简单，用于简化服务间的调用（远程调用）

8. Nacos:  注册中心  **服务注册 服务发现** **配置管理**

9. s

10. 

11. Docker:![image-20250304215947460](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250304215947460.png)

12. 碰到依赖导入错误问题先下载install 

13. 在 Maven 的依赖坐标中，org.example 是默认的 占位符命名，

14. multiply（）常用于BigDecimal的高精度小数 常见金额的计算

15. 配置优先级规则<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250306153857870.png" alt="image-20250306153857870" style="zoom:50%;" />

16. 配置中心 数据隔离<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250306154219637.png" alt="image-20250306154219637" style="zoom: 33%;" />

17. **Nacos的总结**<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250307143047394.png" alt="image-20250307143047394" style="zoom: 33%;" />



### 						OpenFeign

1. .OpenFeign:  Spring cloud远程调用的组件   "**OpenFeign 声明式**的REST客户端"   与"**编程式**的REST客户端 **RestTemplate**"
2. OpenFeign本身不直接实现**负载均衡**逻辑，但它能够与Spring Cloud的负载均衡机制无缝集成，包括使用类似轮询的负载均衡策略。同时，OpenFeign默认带有负载均衡。
3. **Rest客户端**  是使用 RESTful Web 服务的应用程序或工具，主要功能是创建 HTTP 请求，向服务器发送请求并处理响应。
4. <img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250307144050873.png" alt="image-20250307144050873" style="zoom: 25%;" />
5. 常见面试题：客户端与服务端的负载均衡<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250307151356212.png" alt="image-20250307151356212" style="zoom: 50%;" />
6. OpenFeign这个rest客户端，操作简单，无需冗余的配置，并且内部默认与spring cloud的负载均衡配置集成，还有他的进阶用法，超时控制，防止出现服务雪崩的问题  还有重试机制以及请求与响应拦截器  FallBack：客户端的sentinel做熔断的功能打开兜底回调<img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250307154509945.png" alt="image-20250307154509945" style="zoom: 50%;" />
7. **套接字**也就是**socket**：本质上是对 TCP/IP 协议的封装，使开发者能够使用更高层次的接口进行网络编程。
8. **Sentinel** 是阿里巴巴开源的一款高性能的流量控制组件  通过熔断和服务降级来服务保护
9. <img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250310113253317.png" alt="image-20250310113253317" style="zoom: 50%;" />![image-20250310143221345](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250310143221345.png)
10. <img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250310113146211.png" alt="image-20250310113146211" style="zoom: 33%;" />
11. 流控规则：限制多余请求，从而保证系统资源不被耗尽
12. QPS 即每秒查询率（Queries Per Second），是对一个特定的查询服务器在规定时间内所处理流量多少的衡量标准，
13. <img src="C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20250310153407034.png" alt="image-20250310153407034" style="zoom:50%;" />
14. 排队等待的  漏桶算法
15. 除了直接拒绝，关系限流策略会被忽略















1. ```java
   //对象转为json
   private ObjectMapper objectMapper = new ObjectMapper();
   String json = objectMapper.writeValueAsString(r);
   ```








































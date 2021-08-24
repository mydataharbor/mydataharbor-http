# mydataharbor-http-plugin
# 作者

MyDataHarbor([1053618636@qq.com](mailto:1053618636@qq.com))

# 项目介绍

该项目是为MyDataHarbor实现http协议的Sink，让使用者可以将数据通过http发送给下游。

# 实现版本

| 中间件/协议 | 数据源（DataSource） | 写入源（Sink） |
| ----------- | -------------------- | -------------- |
| http        | 暂不考虑             | ✅              |

# 配置

## Sink配置

```java
 @MyDataHarborMarker(title = "需要请求的url地址", require = true)
  private String url;

  @MyDataHarborMarker(title = "连接超时时间", require = false)
  private Integer connectTimeout = 1000;

  @MyDataHarborMarker(title = "读超时时间", require = false)
  private Integer readTimeout = 5000;

  @MyDataHarborMarker(title = "写超时时间", require = false)
  private Integer writeTimeout = 5000;

  @MyDataHarborMarker(title = "最大空闲连接数", require = false)
  private Integer maxIdle = 100;

  @MyDataHarborMarker(title = "存活时间" ,des = "单位：秒", require = false)
  private Integer keepAliveDuration = 30;

  @MyDataHarborMarker(title = "请求打印日志等级", require = false)
  private HttpLoggingInterceptor.Level logLevel = HttpLoggingInterceptor.Level.BASIC;
```


## 服务化最佳实践
- 服务接口，服务模型，服务异常等均放在 API 包中.重用发布等价原则(REP)，共同重用原则(CRP)
- 服务接口尽可能大粒度，每个服务方法应代表一个功能，而不是某功能的一个步骤
- 每个接口都应定义版本号，为后续不兼容升级提供可能.建议使用两位版本号，因为第三位版本号通常表示兼容升级
- 兼容性:服务接口增加方法，或服务模型增加字段，可向后兼容，删除方法或删除字段，将不兼容
- 不建议用 Enum，可以用 String 代替
- 服务参数及返回值建议使用 POJO 对象.服务参数及返回值不建议使用接口，因为数据模型抽象的意义不大.服务参数及返回值都必需是 byValue 的，而不能是 byReference 的，
- 建议使用异常汇报错误，而不是返回错误码,可以通过 override 掉异常类的 fillInStackTrace() 方法为空方法
- 查询方法不建议抛出 checked 异常
- 不应将 DAO 或 SQL 等异常抛给消费方
- 不要只是因为是 Dubbo 调用，而把调用 try...catch 起来. 应该加上合适的回滚边界上。

## 推荐用法
- 配置管理信息,owner,organization
- 配置 Dubbo 缓存文件,会缓存注册中心的列表和服务提供者列表.避免内容覆盖和冲突。
- 在 Provider 配置后，Consumer 不配置则会使用 Provider 的配置值，
即 Provider 配置可以作为 Consumer 的缺省值.Provider 上尽量多配置 Consumer 端的属性
- 不要使用 dubbo.properties 文件配置，推荐使用对应 XML 配置

## 服务提供者暴露过程
![](http://upload-images.jianshu.io/upload_images/1041678-0db0d7dd6fd7a998.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/1041678-f90a214d6083df42.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/1041678-a08cc70f2d564140.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![](http://upload-images.jianshu.io/upload_images/1041678-c47efaec0ba84167.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 集群容错的架构设计图
![](http://upload-images.jianshu.io/upload_images/1041678-7a2a42110a73253a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
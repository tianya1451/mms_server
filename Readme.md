# 中国移动MM7彩信模拟网关

## 更新日志

2014年4月11日下午12:27：    

* 修改脚本java进程不被打断
* 引入google guava 简化代码  
* 引入eventbus异步事件处理状态报告  

2014年4月10日下午3:43：  

* 修改类注释，修改状态报告发送为异步，降低请求响应延时  

##已实现功能如下：
* 彩信接收及响应处理
* 彩信状态报告发送(已实现组包回复多条状态报告)状态报告异步发送
* http长链接支持
* 强制关闭状态报告
* 配置自动更新（修改mmsConfig.properties文件后10秒自动生效，周期可修改）
* 性能数据实时统计

## 性能测试
1. 测试环境：MAC OS 10.9，CPU:I7 4核8线程，内存：8G
2. 速度：80KB彩信包，平均140条每秒

## 注意事项  

  
**对于状态报告接收较慢客户端，本模拟网关会对状态报告进行缓存，1G内存约缓存63W条状态报告，测试情况为组包发送，每包3个手机号，实际使用中可根据情况调整startup.sh脚本中内存参数**
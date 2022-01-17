# What is serverless

#Serverless 服务通常指函数计算，开发人员只需要在服务提供商中上传需要执行的函数代码即可，无需关心服务器配置，容器管理等其他问题。

## 计费方式

以AWS Lambda为例，函数计算服务有以下几种产生费用的方式：

* 持续时间收费，即函数运行的持续时间，使用的时候要注意函数的执行时间，参考[[how-serverless-function-run]]中的使用注意事项。
* 预配置并发，这里和[[how-serverless-function-run]]有关，详情可参考(Lambda 预配置并发介绍)[https://aws.amazon.com/cn/blogs/china/introduction-to-lambda-pre-configured-concurrency/]。
* 数据传输和其他费用，如使用VPC和S3等服务产生的费用
# active mq

## 通信流程
* 启动服务器（集群）
* 通过connectfactory 创建connect
* 创建session
* 根据destination 创建 生产者 和消费者
* 生产消息
* 消费消息

## 通信方式

* topic 形式
  多个生产者，多个消费者
  消费者消费的消息一样，是所有生产者生产的消息总和；后来注册的消费者，注册之前的消息监听不到
* queue 形式
  多个生产者多个消费者
  所有生产者生产的消息总和与所有消费者消费的消息总和一样
  不同消费者消费的消息不同，每个消息只会被一个消费者消费
* request-response 非主要

## 消息种类
* MapMessage 强类型 键值对
* TextMessage 普通文本消息

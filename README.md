
参考文档：https://docs.spring.io/spring-amqp/docs/2.1.5.RELEASE/reference/


#问题：
  1.消息持久化（在broken宕机恢复后,队列中的消息不丢失）
  2.消费者 push 与 pull的区别与实现
  3.消费确认  ACK与NAK
  4.消息的属性设置和有效载荷
  5.Channels 的设置
  6.queue 创建的设置
  7.常用设置类
    ConnectionFactory
    AmqpAdmin
    AmqpTemplate
    
```Java 
   public class Message {
    private final MessageProperties messageProperties;
    private final byte[] body;
  }
```
  
  
    
  

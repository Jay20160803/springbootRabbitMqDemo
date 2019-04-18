
参考文档：https://docs.spring.io/spring-amqp/docs/2.1.5.RELEASE/reference/


#问题：</br>
  >1.消息持久化（在broken宕机恢复后,队列中的消息不丢失) </br>
  2.消费者 push 与 pull的区别与实现</br>
  3.消费确认  ACK与NAK</br>
  4.消息的属性设置和有效载荷</br>
  5.Channels 的设置</br>
  6.queue 创建的设置</br>
  7.常用设置类</br>
    ConnectionFactory</br>
    AmqpAdmin</br>
    AmqpTemplate</br>
    
```Java 
   public class Message {
    private final MessageProperties messageProperties;
    private final byte[] body;
  }
```
  
  
    
  


#Message
```Java 
   public class Message {
    private final MessageProperties messageProperties;
    private final byte[] body;
  }
```

#Exchange：broken中的每个虚拟主机，都有唯一命名的Exchange
>name: exchange 的名称</br>
exchangeType: 
direct: 
topic: 
fanout:
headers:

```Java 
 public interface Exchange {
    String getName();
    String getExchangeType();
    boolean isDurable();
    boolean isAutoDelete();
    Map<String, Object> getArguments();

}
```  

#Queue: Queue类表示消息使用者从其中接收消息的组件
>name: 队列名称</br>
durable：队列是否持久化
exclusive： 
autoDelete：
```java
public class Queue  {

    private final String name;

    private volatile boolean durable;

    private volatile boolean exclusive;

    private volatile boolean autoDelete;

    private volatile Map<String, Object> arguments;

    /**
     * The queue is durable, non-exclusive and non auto-delete.
     *
     * @param name the name of the queue.
     */
    public Queue(String name) {
        this(name, true, false, false);
    }
    // Getters and Setters omitted for brevity

}
```

#Binding 绑定Exchange与Queue
>绑定队列到 DirectExchange,指定routing key
```Java
new Binding(someQueue, someDirectExchange, "foo.bar");
```
绑定队列到 TopicExchange,指定routingKey 配备模式
```Java
new Binding(someQueue, someTopicExchange, "foo.*");
```
绑定队列到 FanoutExchange,不指定routingKey
```Java
new Binding(someQueue, someFanoutExchange);
```

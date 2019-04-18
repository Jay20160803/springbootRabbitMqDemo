
#Message
```Java 
   public class Message {
    private final MessageProperties messageProperties;
    private final byte[] body;
  }
```
#Exchange：broken中的每个虚拟主机，都有唯一命名的Exchange
>name: exchange 的名称
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

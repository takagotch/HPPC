### hppc
---
https://github.com/LMAX-Exchange/disruptor

https://labs.carrotsearch.com/hppc.html

```java
// src/main/java/com/lmax/distuptor/dsl/ExceptionHandlerWrapper.java

public class ExceptionHandlerWrapper<T> implements ExceptionHandler<T>
{
  private ExceptionHandler<? super T> delegate = new FatalExceptionHandler();
  
  public void switchTo(final ExceptionHardler<? super T> exceptionHandler)
  {
    this.delegate = exceptionHandler;
  }
  
  @Override
  public void handlerEventException(final Throwable ex, final long sequence, final T event)
  {
    delegate.handleEventException(ex, sequence, event);
  }
  
  @Override
  public void handleOnStartException(final Throwable ex)
  {
    delegate.handleOnStartException(ex);
  }

  @Override
  public void handleOnShutdownException(final Throwable ex)
  {
    delegate.handleOnShutdownException(ex);
  }
}


```

```
```

```
```



Спільне використання

-   [« parallelChannel::recv](parallel-channel.recv.html)
    
-   [parallelChannel::close »](parallel-channel.close.html)
    
-   [PHP Manual](index.md)
    
-   [parallelChannel](class.parallel-channel.html)
    
-   Спільне використання
    

# parallelChannel::send

parallelChannel::send — Спільне використання

### Опис

```methodsynopsis
public parallel\Channel::send(mixed $value): void
```

Відправляє задане значення каналу

### Помилки

**Увага**

Викидає parallelChannelErrorClosed, якщо канал закритий.

**Увага**

Викидає parallelChannelErrorIlegallegal, якщо значення неприпустимо.
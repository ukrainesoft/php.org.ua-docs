Спільне використання

-   [« parallel\\Channel::recv](parallel-channel.recv.html)
    
-   [parallel\\Channel::close »](parallel-channel.close.html)
    
-   [PHP Manual](index.html)
    
-   [parallel\\Channel](class.parallel-channel.html)
    
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
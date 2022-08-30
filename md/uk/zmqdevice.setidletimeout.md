Встановити час очікування простою

-   [« ZMQDevice::setIdleCallback](zmqdevice.setidlecallback.md)
    
-   [ZMQDevice::setTimerCallback »](zmqdevice.settimercallback.md)
    
-   [PHP Manual](index.md)
    
-   [ZMQDevice](class.zmqdevice.md)
    
-   Встановити час очікування простою
    

# ZMQDevice::setIdleTimeout

(No version information available, might only be in Git)

ZMQDevice::setIdleTimeout — Встановити час очікування простою

### Опис

```methodsynopsis
public ZMQDevice::setIdleTimeout(int $timeout): ZMQDevice
```

Встановлює значення часу очікування запуску callback-функції при простої.

### Список параметрів

`timeout`

Значення у мілісекундах.

### Значення, що повертаються

Повертає поточний об'єкт.
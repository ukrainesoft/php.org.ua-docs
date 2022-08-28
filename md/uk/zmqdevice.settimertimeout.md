Встановити час очікування таймера

-   [« ZMQDevice::setTimerCallback](zmqdevice.settimercallback.html)
    
-   [ZooKeeper »](book.zookeeper.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQDevice](class.zmqdevice.html)
    
-   Встановити час очікування таймера
    

# ZMQDevice::setTimerTimeout

(No version information available, might only be in Git)

ZMQDevice::setTimerTimeout — Встановити час очікування таймера

### Опис

```methodsynopsis
public ZMQDevice::setTimerTimeout(int $timeout): ZMQDevice
```

Встановлює час очікування на таймер. Якщо задана callback-функція по таймеру, вона буде викликатися із заданою частотою. Додано до версії модуля 1.1.0.

### Список параметрів

`timeout`

Значення часу очікування.

### Значення, що повертаються

Повертає поточний об'єкт.
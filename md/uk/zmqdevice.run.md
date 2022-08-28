Запуск нового пристрою

-   [« ZMQDevice::getTimerTimeout](zmqdevice.gettimertimeout.html)
    
-   [ZMQDevice::setIdleCallback »](zmqdevice.setidlecallback.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQDevice](class.zmqdevice.html)
    
-   Запуск нового пристрою
    

# ZMQDevice::run

(No version information available, might only be in Git)

ZMQDevice::run — Запуск нового пристрою

### Опис

```methodsynopsis
public ZMQDevice::run(): void
```

Запускає пристрій.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Запуск цього методу блокує виконання, поки пристрій запущено. Не рекомендується використовувати в інтерактивних сценаріях. У разі помилки викидає виняток ZMQDeviceException.
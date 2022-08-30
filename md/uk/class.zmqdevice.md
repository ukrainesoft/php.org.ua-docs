Клас ZMQDevice

-   [« ZMQPoll::remove](zmqpoll.remove.md)
    
-   [ZMQDevice::construct »](zmqdevice.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Обмін повідомленнями 0MQ](book.zmq.md)
    
-   Клас ZMQDevice
    

# Клас ZMQDevice

(PECL zmq >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ZMQDevice
     
     {
    

    /* Методы */
    
   public __construct(ZMQSocket $frontend, ZMQSocket $backend, ZMQSocket $listener = ?)
public getIdleTimeout(): ZMQDevice
public getTimerTimeout(): ZMQDevice
public run(): void
public setIdleCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
public setIdleTimeout(int $timeout): ZMQDevice
public setTimerCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
public setTimerTimeout(int $timeout): ZMQDevice

   }
```

## Зміст

-   [ZMQDevice::construct](zmqdevice.construct.md) — Створює новий пристрій
-   [ZMQDevice::getIdleTimeout](zmqdevice.getidletimeout.md) — Отримати час очікування бездіяльності
-   [ZMQDevice::getTimerTimeout](zmqdevice.gettimertimeout.md) - Отримати час очікування таймера
-   [ZMQDevice::run](zmqdevice.run.md) — Запуск нового пристрою
-   [ZMQDevice::setIdleCallback](zmqdevice.setidlecallback.md) - Встановити callback-функцію бездіяльності
-   [ZMQDevice::setIdleTimeout](zmqdevice.setidletimeout.md) — Встановити час очікування простою
-   [ZMQDevice::setTimerCallback](zmqdevice.settimercallback.md) - Встановити callback-функцію за таймером
-   [ZMQDevice::setTimerTimeout](zmqdevice.settimertimeout.md) - Встановити час очікування таймера
Клас ZMQDevice

-   [« ZMQPoll::remove](zmqpoll.remove.html)
    
-   [ZMQDevice::construct »](zmqdevice.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Обмін повідомленнями 0MQ](book.zmq.html)
    
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

-   [ZMQDevice::construct](zmqdevice.construct.html) — Створює новий пристрій
-   [ZMQDevice::getIdleTimeout](zmqdevice.getidletimeout.html) — Отримати час очікування бездіяльності
-   [ZMQDevice::getTimerTimeout](zmqdevice.gettimertimeout.html) - Отримати час очікування таймера
-   [ZMQDevice::run](zmqdevice.run.html) — Запуск нового пристрою
-   [ZMQDevice::setIdleCallback](zmqdevice.setidlecallback.html) - Встановити callback-функцію бездіяльності
-   [ZMQDevice::setIdleTimeout](zmqdevice.setidletimeout.html) — Встановити час очікування простою
-   [ZMQDevice::setTimerCallback](zmqdevice.settimercallback.html) - Встановити callback-функцію за таймером
-   [ZMQDevice::setTimerTimeout](zmqdevice.settimertimeout.html) - Встановити час очікування таймера
Встановити callback-функцію за таймером

-   [« ZMQDevice::setIdleTimeout](zmqdevice.setidletimeout.md)
    
-   [ZMQDevice::setTimerTimeout »](zmqdevice.settimertimeout.md)
    
-   [PHP Manual](index.md)
    
-   [ZMQDevice](class.zmqdevice.md)
    
-   Встановити callback-функцію за таймером
    

# ZMQ Device::setTimer Callback

(No version information available, might only be in Git)

ZMQDevice::setTimerCallback — Встановити callback-функцію за таймером

### Опис

```methodsynopsis
public ZMQDevice::setTimerCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
```

Встановлює callback-функцію за таймером. Періодично запускає callback-функцію. Від callback-функції простою відрізняється тим, що запускається в будь-якому випадку, а не тільки при простому пристрої. Сигнатура функції - (mixed $userdata). Додано у версії 1.1.0.

### Список параметрів

`cb_func`

Callback-функція для запуску за таймером. Повернення **`false`** або значення, яке наводиться до **`false`** призведе до зупинки пристрою.

`timeout`

Час очікування у мілісекундах. Callback-функція буде викликатись через задані проміжки часу. Гарантує, що між запусками функції відбуватиметься не менше заданої кількості мілісекунд.

`user_data`

Додаткові дані, які передаватимуться в callback-функцію.

### Значення, що повертаються

Повертає поточний об'єкт.
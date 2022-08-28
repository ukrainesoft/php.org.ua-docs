Встановити callback-функцію бездіяльності

-   [« ZMQDevice::run](zmqdevice.run.html)
    
-   [ZMQDevice::setIdleTimeout »](zmqdevice.setidletimeout.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQDevice](class.zmqdevice.html)
    
-   Встановити callback-функцію бездіяльності
    

# ZMQ Device::set Idle Callback

(No version information available, might only be in Git)

ZMQDevice::setIdleCallback — Встановити callback-функцію бездіяльності

### Опис

```methodsynopsis
public ZMQDevice::setIdleCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
```

Встановлює callback-функцію бездіяльності. Якщо задано час очікування простою, ця функція буде запущена, якщо цикл опитування не отримає жодної події протягом цього часу. Якщо функція поверне ефективне **`false`**, пристрій буде зупинено. Сигнатура функції - (mixed $userdata).

### Список параметрів

`cb_func`

Callback-функція для запуску у разі тривалого простою. Повернення **`false`** або значення, яке наводиться до **`false`** призведе до зупинки пристрою.

`timeout`

Час очікування простою у мілісекундах. Callback-функція буде викликатись кожного разу, коли протягом заданого часу не відбуватиметься жодних подій. Гарантується, що між запусками функції відбуватиметься не менше заданої кількості мілісекунд.

`user_data`

Додаткові дані, які передаватимуться в callback-функцію.

### Значення, що повертаються

У разі успішного виконання поточний об'єкт повертає.
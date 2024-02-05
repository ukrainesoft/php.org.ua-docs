---
navigation:
  - zmqdevice.run.md: '« ZMQDevice::run'
  - zmqdevice.setidletimeout.md: 'ZMQDevice::setIdleTimeout »'
  - index.md: PHP Manual
  - class.zmqdevice.md: ZMQDevice
title: 'ZMQDevice::setIdleCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQDevice::setIdleCallback

(No version information available, might only be in Git)

ZMQDevice::setIdleCallback — Встановити callback-функцію бездіяльності

### Опис

```methodsynopsis
public ZMQDevice::setIdleCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
```

Встановлює callback-функцію бездіяльності. Якщо задано час очікування простою, то ця функція буде запущена, якщо цикл опитування не отримає жодної події протягом цього часу. Якщо функція поверне ефективне **`false`**, пристрій буде зупинено. Сигнатура функції - (mixed $user\_data).

### Список параметрів

`cb_func`

Callback-функція для запуску у разі тривалого простою. Повернення **`false`** або значення, яке наводиться до **`false`** призведе до зупинки пристрою.

`timeout`

Час очікування простою у мілісекундах. Callback-функція буде викликатись кожного разу, коли протягом заданого часу не відбуватиметься жодних подій. Гарантується, що між запусками функції відбуватиметься не менше заданої кількості мілісекунд.

`user_data`

Додаткові дані, які передаватимуться в callback-функцію.

### Значення, що повертаються

У разі успішного виконання поточний об'єкт повертає.

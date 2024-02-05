---
navigation:
  - zmqdevice.setidletimeout.md: '« ZMQDevice::setIdleTimeout'
  - zmqdevice.settimertimeout.md: 'ZMQDevice::setTimerTimeout »'
  - index.md: PHP Manual
  - class.zmqdevice.md: ZMQDevice
title: 'ZMQDevice::setTimerCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQDevice::setTimerCallback

(No version information available, might only be in Git)

ZMQDevice::setTimerCallback — Встановити callback-функцію за таймером

### Опис

```methodsynopsis
public ZMQDevice::setTimerCallback(callable $cb_func, int $timeout, mixed $user_data = ?): ZMQDevice
```

Встановлює callback-функцію за таймером. Періодично запускає callback-функцію. Від callback-функції простою відрізняється тим, що запускається в будь-якому випадку, а не тільки при простому пристрої. Сигнатура функції - (mixed $user\_data). Додано у версії 1.1.0.

### Список параметрів

`cb_func`

Callback-функция для запуска по таймеру. Возврат\*\*`false`\*\* або значення, яке наводиться до **`false`** призведе до зупинки пристрою.

`timeout`

Час очікування у мілісекундах. Callback-функція буде викликатись через задані проміжки часу. Гарантує, що між запусками функції відбуватиметься не менше заданої кількості мілісекунд.

`user_data`

Додаткові дані, які передаватимуться в callback-функцію.

### Значення, що повертаються

Повертає поточний об'єкт.

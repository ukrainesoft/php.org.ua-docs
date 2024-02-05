---
navigation:
  - zmqdevice.gettimertimeout.md: '« ZMQDevice::getTimerTimeout'
  - zmqdevice.setidlecallback.md: 'ZMQDevice::setIdleCallback »'
  - index.md: PHP Manual
  - class.zmqdevice.md: ZMQDevice
title: 'ZMQDevice::run'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

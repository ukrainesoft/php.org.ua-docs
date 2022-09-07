---
navigation:
  - zmqdevice.setidlecallback.md: '« ZMQDevice::setIdleCallback'
  - zmqdevice.settimercallback.md: 'ZMQDevice::setTimerCallback »'
  - index.md: PHP Manual
  - class.zmqdevice.md: ZMQDevice
title: 'ZMQDevice::setIdleTimeout'
---
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

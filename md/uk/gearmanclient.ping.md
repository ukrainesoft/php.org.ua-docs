---
navigation:
  - gearmanclient.jobstatus.md: '« GearmanClient::jobStatus'
  - gearmanclient.removeoptions.md: 'GearmanClient::removeOptions »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::ping'
---
# GearmanClient::ping

(No version information available, might only be in Git)

GearmanClient::ping — Надсилає дані на всі сервери, щоб перевірити, які з них виведуть ці дані

### Опис

```methodsynopsis
public GearmanClient::ping(string $workload): bool
```

Посилає дані на всі сервери та визначає, які з них виведуть ці дані у вихідний потік. Надіслані дані не обробляються. Метод використовується для тестування та налагодження.

### Список параметрів

`workload`

Дані, які можна вивести у вихідний потік.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

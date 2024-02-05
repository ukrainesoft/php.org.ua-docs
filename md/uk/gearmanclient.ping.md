---
navigation:
  - gearmanclient.jobstatus.md: '« GearmanClient::jobStatus'
  - gearmanclient.removeoptions.md: 'GearmanClient::removeOptions »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::ping'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

---
navigation:
  - function.ssh2-connect.md: « ssh2\_connect
  - function.ssh2-exec.md: ssh2\_exec »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_disconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_disconnect

(PECL ssh2 >= 1.0)

ssh2\_disconnect — Закрити з'єднання з віддаленим сервером SSH

### Опис

```methodsynopsis
ssh2_disconnect(resource $session): bool
```

Закрити з'єднання з віддаленим сервером SSH.

### Список параметрів

`session`

Ідентифікатор посилання з'єднання SSH, отриманий в результаті виклику [ssh2\_connect()](function.ssh2-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ssh2\_connect()](function.ssh2-connect.md) \- Підключення до SSH-сервера

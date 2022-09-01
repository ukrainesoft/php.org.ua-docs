---
navigation:
  - function.ssh2-connect.html: « ssh2connect
  - function.ssh2-exec.html: ssh2exec »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2disconnect
---
# ssh2disconnect

(PECL ssh2 >= 1.0)

ssh2disconnect — Закрити з'єднання з віддаленим сервером SSH

### Опис

```methodsynopsis
ssh2_disconnect(resource $session): bool
```

Закрити з'єднання з віддаленим сервером SSH.

### Список параметрів

`session`

Ідентифікатор посилання з'єднання SSH, отриманий в результаті виклику [ssh2connect()](function.ssh2-connect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ssh2connect()](function.ssh2-connect.html) - Підключення до SSH-сервера

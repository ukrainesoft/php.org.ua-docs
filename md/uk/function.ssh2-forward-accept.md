---
navigation:
  - function.ssh2-fingerprint.html: « ssh2fingerprint
  - function.ssh2-forward-listen.html: ssh2forwardlisten »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2forwardaccept
---
# ssh2forwardaccept

(PECL ssh2> = 0.9.0)

ssh2forwardaccept — Приймає з'єднання, створене слухачем

### Опис

```methodsynopsis
ssh2_forward_accept(resource $listener): resource|false
```

Приймає з'єднання, створене слухачем.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`desc`

Ресурс SSH2 Listener, отриманий у результаті виклику [ssh2forwardlisten()](function.ssh2-forward-listen.html)

### Значення, що повертаються

Повертає ресурс потоку або **`false`** у разі виникнення помилки.

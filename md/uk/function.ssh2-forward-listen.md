---
navigation:
  - function.ssh2-forward-accept.md: « ssh2forwardaccept
  - function.ssh2-methods-negotiated.md: ssh2methodsnegotiated »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2forwardlisten
---
# ssh2forwardlisten

(PECL ssh2> = 0.9.0)

ssh2forwardlisten — Зв'язує порт на віддаленому сервері та прослуховує з'єднання

### Опис

```methodsynopsis
ssh2_forward_listen(    resource $session,    int $port,    string $host = ?,    int $max_connections = 16): resource|false
```

Зв'язує порт на віддаленому сервері та прослуховує з'єднання.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`session`

Ресурс SSH Session, отриманий через виклик [ssh2connect()](function.ssh2-connect.md)

`port`

Порт віддаленого сервера.

`host`

`max_connections`

### Значення, що повертаються

Повертає SSH2 Listener або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ssh2forwardaccept()](function.ssh2-forward-accept.md) - приймає з'єднання, створене слухачем

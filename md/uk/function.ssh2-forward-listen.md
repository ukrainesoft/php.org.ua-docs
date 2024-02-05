---
navigation:
  - function.ssh2-forward-accept.md: « ssh2\_forward\_accept
  - function.ssh2-methods-negotiated.md: ssh2\_methods\_negotiated »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_forward\_listen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_forward\_listen

(PECL ssh2 >= 0.9.0)

ssh2\_forward\_listen — Зв'язує порт на віддаленому сервері та прослуховує з'єднання

### Опис

```methodsynopsis
ssh2_forward_listen(    resource $session,    int $port,    string $host = ?,    int $max_connections = 16): resource|false
```

Зв'язує порт на віддаленому сервері та прослуховує з'єднання.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`session`

Ресурс SSH Session, отриманий у результаті виклику [ssh2\_connect()](function.ssh2-connect.md)

`port`

Порт віддаленого сервера.

`host`

`max_connections`

### Значення, що повертаються

Возвращает SSH2 Listener или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ssh2\_forward\_accept()](function.ssh2-forward-accept.md) \- приймає з'єднання, створене слухачем

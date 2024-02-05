---
navigation:
  - function.ssh2-fingerprint.md: « ssh2\_fingerprint
  - function.ssh2-forward-listen.md: ssh2\_forward\_listen »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_forward\_accept
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_forward\_accept

(PECL ssh2 >= 0.9.0)

ssh2\_forward\_accept — Приймає з'єднання, створене слухачем

### Опис

```methodsynopsis
ssh2_forward_accept(resource $listener): resource|false
```

Приймає з'єднання, створене слухачем.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`desc`

Ресурс SSH2 Listener, отриманий у результаті виклику [ssh2\_forward\_listen()](function.ssh2-forward-listen.md)

### Значення, що повертаються

Повертає ресурс потоку або \*\*`false`\*\*в случае возникновения ошибки.

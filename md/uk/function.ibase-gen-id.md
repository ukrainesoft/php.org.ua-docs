---
navigation:
  - function.ibase-free-result.html: « ibasefreeresult
  - function.ibase-maintain-db.html: ibasemaintaindb »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseгенід
---
# ibaseгенід

(PHP 5, PHP 7 < 7.4.0)

ibaseгенid — Збільшує вказаний генератор та повертає його нове значення

### Опис

```methodsynopsis
ibase_gen_id(string $generator, int $increment = 1, resource $link_identifier = null): mixed
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Значення, що повертаються

Повертає нове значення генератора у вигляді цілого чи рядка, якщо значення занадто велике.

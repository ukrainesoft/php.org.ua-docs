---
navigation:
  - function.ibase-gen-id.md: « ibasegenід
  - function.ibase-modify-user.md: ibasemodifyuser »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasemaintainдб
---
# ibasemaintainдб

(PHP 5, PHP 7 < 7.4.0)

ibasemaintaindb — Виконує команду обслуговування на сервері бази даних

### Опис

```methodsynopsis
ibase_maintain_db(    resource $service_handle,    string $db,    int $action,    int $argument = 0): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

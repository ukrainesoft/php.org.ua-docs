---
navigation:
  - ref.radius.md: « Функції Radius
  - function.radius-add-server.md: radius\_add\_server »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_acct\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_acct\_open

(PECL radius >= 1.1.0)

radius\_acct\_open — Створює дескриптор Radius для обліку

### Опис

```methodsynopsis
radius_acct_open(): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор у разі успішного виконання або **`false`** у разі виникнення помилки. Функція завершиться з помилкою, лише якщо недостатньо пам'яті.

### Приклади

**Приклад #1 Приклад використання** radius\_acct\_open()\*\*\*\*

```php
<?php
$res = radius_acct_open ()
    or die ("Не удалось создать дескриптор");
print("Дескриптор успешно создан");
?>
```

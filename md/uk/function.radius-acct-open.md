---
navigation:
  - ref.radius.md: « Функции Radius
  - function.radius-add-server.md: radiusaddserver »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusacctopen
---
# radiusacctopen

(PECL radius >= 1.1.0)

radiusacctopen — Створює дескриптор Radius для обліку

### Опис

```methodsynopsis
radius_acct_open(): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор у разі успішного виконання або **`false`** у разі виникнення помилки. Функція завершиться з помилкою, лише якщо недостатньо пам'яті.

### Приклади

**Приклад #1 Приклад використання **radiusacctopen()****

```php
<?php
$res = radius_acct_open ()
    or die ("Не удалось создать дескриптор");
print("Дескриптор успешно создан");
?>
```

---
navigation:
  - function.radius-add-server.md: « radius\_add\_server
  - function.radius-close.md: radius\_close »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_auth\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_auth\_open

(PECL radius >= 1.1.0)

radius\_auth\_open — Створює дескриптор Radius для автентифікації

### Опис

```methodsynopsis
radius_auth_open(): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає дескриптор у разі успішного виконання або **`false`** у разі виникнення помилки. Функція завершиться з помилкою, лише якщо недостатньо пам'яті.

### Приклади

**Пример #1 Пример использования**radius\_auth\_open()\*\*\*\*

```php
<?php
$radh = radius_auth_open()
    or die ("Не удалось создать дескриптор");
echo "Дескриптор успешно создан";
?>
```

---
navigation:
  - ref.mail.md: « Пошта
  - function.mail.md: mail »
  - index.md: PHP Manual
  - ref.mail.md: Пошта
title: ezmlm\_hash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ezmlm\_hash

(PHP 4 >= 4.0.2, PHP 5, PHP 7)

ezmlm\_hash — обчислює хеш-суму, необхідну для EZMLM

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
ezmlm_hash(string $addr): int
```

**ezmlm\_hash()** обчислює хеш-суму, необхідну для зберігання поштових списків EZMLM у базі MySQL.

### Список параметрів

`addr`

Хешована адреса електронної пошти.

### Значення, що повертаються

Хеш-сумма параметра`addr`

### Приклади

**Приклад #1 Обчислює хеш-суму та підписка користувача на будь-що**

```php
<?php

$user = "joecool@example.com";
$hash = ezmlm_hash($user);
$query = sprintf("INSERT INTO sample VALUES (%s, '%s')", $hash, $user);
$db->query($query); // используя интерфейс PHPLIB db

?>
```

Обчислює хеш-суму, необхідну для EZMLM

-   [« Почта](ref.mail.md)
    
-   [mail »](function.mail.md)
    
-   [PHP Manual](index.md)
    
-   [Почта](ref.mail.md)
    
-   Обчислює хеш-суму, необхідну для EZMLM
    

# ezmlmhash

(PHP 4> = 4.0.2, PHP 5, PHP 7)

ezmlmhash — обчислює хеш-суму, необхідну для EZMLM

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
ezmlm_hash(string $addr): int
```

**ezmlmhash()** обчислює хеш-суму, необхідну для зберігання поштових списків EZMLM в базі MySQL.

### Список параметрів

`addr`

Хешована адреса електронної пошти.

### Значення, що повертаються

Хеш-сума параметра `addr`

### Приклади

**Приклад #1 Обчислює хеш-суму та підписка користувача на будь-що**

```php
<?php

$user = "joecool@example.com";
$hash = ezmlm_hash($user);
$query = sprintf("INSERT INTO sample VALUES (%s, '%s')", $hash, $user);
$db->query($query); // используя интерфейс PHPLIB db

?>
```
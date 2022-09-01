---
navigation:
  - function.cubrid-db-name.html: « cubridдбname
  - function.cubrid-error.html: cubriderror »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubriderrno
---
# cubriderrno

(PECL CUBRID >= 8.3.1)

cubriderrno - Повертає код помилки попередньої операції CUBRID

### Опис

```methodsynopsis
cubrid_errno(resource $conn_identifier = ?): int
```

Повертає код помилки попередньої операції CUBRID.

Функція **cubriderrno()** використовується для отримання коду помилки, що відбулася. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubridconnect()](function.cubrid-connect.md) з'єднання.

### Значення, що повертаються

Код помилки, що виникла, або `0` (нуль), якщо помилки не було.

### Приклади

**Приклад #1 Приклад використання **cubriderrno()****

```php
<?php
$con = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$req = cubrid_execute($con, "select id, name from person");
if ($req) {
    while (list ($id, $name) = cubrid_fetch($req))
    echo $id, $name;
} else {
    echo "Код ошибки: ", cubrid_errno($con);
    echo "Текст ошибки: ", cubrid_error($con);
}
?>
```

Результат виконання цього прикладу:

```
Код ошибки: -493 Текст ошибки: Syntax: Unknown class "person". select id, [name] from person
```

### Дивіться також

-   [cubriderror()](function.cubrid-error.md) - Повертає текст останньої помилки, що відбулася.
-   [cubriderrorcode()](function.cubrid-error-code.md) - Отримати код помилки
-   [cubriderrormsg()](function.cubrid-error-msg.md) - Повертає текст останньої помилки, що відбулася.

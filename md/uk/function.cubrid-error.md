---
navigation:
  - function.cubrid-errno.md: « cubrid\_errno
  - function.cubrid-fetch-array.md: cubrid\_fetch\_array »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_error

(PECL CUBRID >= 8.3.1)

cubrid\_error — Повертає текст останньої помилки, що сталася.

### Опис

```methodsynopsis
cubrid_error(resource $connection = ?): string
```

Функция**cubrid\_error()** використовується для отримання тексту помилки, що відбулася. Зазвичай ви можете отримати текст помилки, якщо якась функція повернула **`false`**

### Список параметрів

`connection`

Ідентифікатор з'єднання.

### Значення, що повертаються

Текст помилки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_error()\*\*\*\*

```php
<?php
$con = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$req = cubrid_execute($con, "select id, name from person");
if ($req) {
    while (list ($id, $name) = cubrid_fetch($req))
    echo $id, $name;
} else {
    echo "Код ошибки: ", cubrid_errno($con);
    echo "Текст ошибки: ", cubrid_error($con);
}
?>
```

Результат виконання наведеного прикладу:

```
Код ошибки: -493 Текст ошибки: Syntax: Unknown class "person". select id, [name] from person
```

### Дивіться також

-   [cubrid\_errno()](function.cubrid-errno.md) \- Повертає код помилки попередньої операції CUBRID
-   [cubrid\_error\_code()](function.cubrid-error-code.md) \- Отримати код помилки
-   [cubrid\_error\_msg()](function.cubrid-error-msg.md) \- Повертає текст останньої помилки, що відбулася.

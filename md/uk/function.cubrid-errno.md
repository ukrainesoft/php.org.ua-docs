---
navigation:
  - function.cubrid-db-name.md: « cubrid\_db\_name
  - function.cubrid-error.md: cubrid\_error »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_errno

(PECL CUBRID >= 8.3.1)

cubrid\_errno - Повертає код помилки попередньої операції CUBRID

### Опис

```methodsynopsis
cubrid_errno(resource $conn_identifier = ?): int
```

Повертає код помилки попередньої операції CUBRID.

Функция**cubrid\_errno()** використовується для отримання коду помилки, що відбулася. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.md)соединение.

### Значення, що повертаються

Код помилки, що виникла, або (нуль), якщо помилки не було.

### Приклади

**Пример #1 Пример использования**cubrid\_errno()\*\*\*\*

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

-   [cubrid\_error()](function.cubrid-error.md) \- Повертає текст останньої помилки, що відбулася.
-   [cubrid\_error\_code()](function.cubrid-error-code.md) \- Отримати код помилки
-   [cubrid\_error\_msg()](function.cubrid-error-msg.md) \- Повертає текст останньої помилки, що відбулася.

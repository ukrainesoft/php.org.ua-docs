Повертає текст останньої помилки, що сталася

-   [« cubrid\_errno](function.cubrid-errno.html)
    
-   [cubrid\_fetch\_array »](function.cubrid-fetch-array.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Повертає текст останньої помилки, що сталася
    

# cubriderror

(PECL CUBRID >= 8.3.1)

cubriderror — Повертає текст останньої помилки, що сталася.

### Опис

```methodsynopsis
cubrid_error(resource $connection = ?): string
```

Функція **cubriderror()** використовується для отримання тексту помилки, що відбулася. Зазвичай ви можете отримати текст помилки, якщо якась функція повернула **`false`**

### Список параметрів

`connection`

Ідентифікатор з'єднання.

### Значення, що повертаються

Текст помилки.

### Приклади

**Приклад #1 Приклад використання **cubriderror()****

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

-   [cubrid\_errno()](function.cubrid-errno.html) - Повертає код помилки попередньої операції CUBRID
-   [cubrid\_error\_code()](function.cubrid-error-code.html) - Отримати код помилки
-   [cubrid\_error\_msg()](function.cubrid-error-msg.html) - Повертає текст останньої помилки, що відбулася.
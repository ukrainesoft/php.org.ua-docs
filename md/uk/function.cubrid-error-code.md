Отримати код помилки

-   [« cubrid\_error\_code\_facility](function.cubrid-error-code-facility.html)
    
-   [cubrid\_error\_msg »](function.cubrid-error-msg.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримати код помилки
    

# cubriderrorcode

(PECL CUBRID >= 8.3.0)

cubriderrorcode — Отримати код помилки

### Опис

```methodsynopsis
cubrid_error_code(): int
```

Функція **cubriderrorcode()** використовується для отримання коду помилки, що відбулася. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Код помилки, що виникла, або `0` (нуль), якщо помилки не було.

### Приклади

**Приклад #1 Приклад використання **cubriderrorcode()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_prepare($conn , "SELECT * FROM code WHERE s_name=?");

$req = @cubrid_execute($req);
if (!$req) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n",
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

Результат виконання цього прикладу:

```
Error facility: 4
Error code: -30015
Error msg: Some parameter not binded
```

### Дивіться також

-   [cubrid\_error\_code\_facility()](function.cubrid-error-code-facility.html) - Отримати код рівня, на якому сталася помилка
-   [cubrid\_error\_msg()](function.cubrid-error-msg.html) - Повертає текст останньої помилки, що відбулася.
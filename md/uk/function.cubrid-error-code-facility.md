Отримати код рівня, на якому сталася помилка

-   [« cubrid\_drop](function.cubrid-drop.html)
    
-   [cubrid\_error\_code »](function.cubrid-error-code.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримати код рівня, на якому сталася помилка
    

# cubriderrorcodefacility

(PECL CUBRID >= 8.3.0)

cubriderrorcodefacility — Отримати код рівня, на якому сталася помилка

### Опис

```methodsynopsis
cubrid_error_code_facility(): int
```

Функція **cubriderrorcodefacility()** використовується виявлення, якому рівні сталася помилка. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Коди рівнів: **`CUBRID_FACILITY_DBMS`** **`CUBRID_FACILITY_CAS`** **`CUBRID_FACILITY_CCI`** **`CUBRID_FACILITY_CLIENT`**

### Приклади

**Приклад #1 Приклад використання **cubriderrorcodefacility()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = @cubrid_execute($conn, "SELECT * FROM unknown");
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
Error facility: 1
Error code: -493
Error msg: Syntax: In line 1, column 15 before END OF STATEMENT
Syntax error: unexpected 'unknown'
```

### Дивіться також

-   [cubrid\_error\_code()](function.cubrid-error-code.html) - Отримати код помилки
-   [cubrid\_error\_msg()](function.cubrid-error-msg.html) - Повертає текст останньої помилки, що відбулася.
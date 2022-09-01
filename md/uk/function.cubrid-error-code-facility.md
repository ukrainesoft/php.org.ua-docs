---
navigation:
  - function.cubrid-drop.html: « cubriddrop
  - function.cubrid-error-code.html: cubriderrorcode »
  - index.html: PHP Manual
  - ref.cubrid.html: Функции CUBRID
title: cubriderrorcodefacility
---
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

-   [cubriderrorcode()](function.cubrid-error-code.md) - Отримати код помилки
-   [cubriderrormsg()](function.cubrid-error-msg.md) - Повертає текст останньої помилки, що відбулася.

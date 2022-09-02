---
navigation:
  - function.cubrid-error-code.md: « cubriderrorcode
  - function.cubrid-execute.md: cubridexecute »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubriderrormsg
---
# cubriderrormsg

(PECL CUBRID >= 8.3.0)

cubriderrormsg — Повертає текст останньої помилки, що відбулася.

### Опис

```methodsynopsis
cubrid_error_msg(): string
```

Функція **cubriderrormsg()** використовується для отримання тексту помилки, що відбулася. Зазвичай ви можете отримати текст помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текст помилки.

### Приклади

**Приклад #1 Приклад використання **cubriderrormsg()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

if (!@cubrid_schema($conn, 100000)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n",
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

Результат виконання цього прикладу:

```
Error facility: 2
Error code: -10015
Error msg: Invalid T_CCI_SCH_TYPE value
```

### Дивіться також

-   [cubriderrorcode()](function.cubrid-error-code.md) - Отримати код помилки
-   [cubriderrorcodefacility()](function.cubrid-error-code-facility.md) - Отримати код рівня, на якому сталася помилка

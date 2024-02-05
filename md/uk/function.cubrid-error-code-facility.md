---
navigation:
  - function.cubrid-drop.md: « cubrid\_drop
  - function.cubrid-error-code.md: cubrid\_error\_code »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_error\_code\_facility
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_error\_code\_facility

(PECL CUBRID >= 8.3.0)

cubrid\_error\_code\_facility — Отримати код рівня, на якому сталася помилка

### Опис

```methodsynopsis
cubrid_error_code_facility(): int
```

Функция**cubrid\_error\_code\_facility()** використовується виявлення, якому рівні сталася помилка. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Коди рівнів: **`CUBRID_FACILITY_DBMS`** **`CUBRID_FACILITY_CAS`** **`CUBRID_FACILITY_CCI`** **`CUBRID_FACILITY_CLIENT`**

### Приклади

**Приклад #1 Приклад використання** cubrid\_error\_code\_facility()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = @cubrid_execute($conn, "SELECT * FROM unknown");
if (!$req) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n",
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

Результат виконання наведеного прикладу:

```
Error facility: 1
Error code: -493
Error msg: Syntax: In line 1, column 15 before END OF STATEMENT
Syntax error: unexpected 'unknown'
```

### Дивіться також

-   [cubrid\_error\_code()](function.cubrid-error-code.md) \- Отримати код помилки
-   [cubrid\_error\_msg()](function.cubrid-error-msg.md) \- Повертає текст останньої помилки, що відбулася.

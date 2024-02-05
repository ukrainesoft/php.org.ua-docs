---
navigation:
  - function.cubrid-error-code.md: « cubrid\_error\_code
  - function.cubrid-execute.md: cubrid\_execute »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_error\_msg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_error\_msg

(PECL CUBRID >= 8.3.0)

cubrid\_error\_msg — Повертає текст останньої помилки, що відбулася.

### Опис

```methodsynopsis
cubrid_error_msg(): string
```

Функция**cubrid\_error\_msg()** використовується для отримання тексту помилки, що відбулася. Зазвичай ви можете отримати текст помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текст помилки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_error\_msg()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

if (!@cubrid_schema($conn, 100000)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n",
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

Результат виконання наведеного прикладу:

```
Error facility: 2
Error code: -10015
Error msg: Invalid T_CCI_SCH_TYPE value
```

### Дивіться також

-   [cubrid\_error\_code()](function.cubrid-error-code.md) \- Отримати код помилки
-   [cubrid\_error\_code\_facility()](function.cubrid-error-code-facility.md) \- Отримати код рівня, на якому сталася помилка

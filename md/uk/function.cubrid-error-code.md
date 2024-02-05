---
navigation:
  - function.cubrid-error-code-facility.md: « cubrid\_error\_code\_facility
  - function.cubrid-error-msg.md: cubrid\_error\_msg »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_error\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_error\_code

(PECL CUBRID >= 8.3.0)

cubrid\_error\_code — Отримати код помилки

### Опис

```methodsynopsis
cubrid_error_code(): int
```

Функция**cubrid\_error\_code()** використовується для отримання коду помилки, що відбулася. Зазвичай ви можете отримати код помилки, якщо якась функція повернула **`false`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Код помилки, що виникла, або (нуль), якщо помилки не було.

### Приклади

**Приклад #1 Приклад використання** cubrid\_error\_code()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_prepare($conn , "SELECT * FROM code WHERE s_name=?");

$req = @cubrid_execute($req);
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
Error facility: 4
Error code: -30015
Error msg: Some parameter not binded
```

### Дивіться також

-   [cubrid\_error\_code\_facility()](function.cubrid-error-code-facility.md) \- Отримати код рівня, на якому сталася помилка
-   [cubrid\_error\_msg()](function.cubrid-error-msg.md) \- Повертає текст останньої помилки, що відбулася.

---
navigation:
  - function.apache-get-version.md: « apache\_get\_version
  - function.apache-lookup-uri.md: apache\_lookup\_uri »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_getenv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_getenv

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

apache\_getenv — Повертає змінну оточення підпроцесу сервера Apache

### Опис

```methodsynopsis
apache_getenv(string $variable, bool $walk_to_top = false): string|false
```

Повертає змінну оточення сервера Apache, вказану параметром `variable`

### Список параметрів

`variable`

Змінне оточення сервера Apache

`walk_to_top`

Отримати змінну верхнього рівня, доступну для всіх рівнів Apache сервера чи ні.

### Значення, що повертаються

Значення змінної оточення сервера Apache у разі успішного виконання, або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apache\_getenv()\*\*\*\*

Нижче наведений приклад показує, як можна отримати значення змінної оточення сервера Apache SERVER\_ADDR.

```php
<?php
$ret = apache_getenv("SERVER_ADDR");
echo $ret;
?>
```

Висновок наведеного прикладу буде схожим на:

```
42.24.42.240
```

### Дивіться також

-   [apache\_setenv()](function.apache-setenv.md) \- Встановлює змінну subprocess\_env Apache
-   [getenv()](function.getenv.md) \- набуває значення однієї чи всіх змінних оточення
-   "[Суперглобальні змінні](language.variables.superglobals.md)"

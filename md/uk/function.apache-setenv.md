---
navigation:
  - function.apache-response-headers.md: « apache\_response\_headers
  - function.getallheaders.md: getallheaders »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_setenv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_setenv

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

apache\_setenv - Встановлює змінну subprocess\_env Apache

### Опис

```methodsynopsis
apache_setenv(string $variable, string $value, bool $walk_to_top = false): bool
```

**apache\_setenv()** встановлює значення змінної оточення Apache, визначеної як `variable`

> **Зауваження** :
> 
> При встановленні змінної оточення Apache, відповідна їй змінна [$\_SERVER](reserved.variables.server.md)не изменяется.

### Список параметрів

`variable`

Змінне оточення, яке потрібно встановити.

`value`

Новое значение переменной`variable`

`walk_to_top`

Чи робити доступною змінну для всіх рівнів Apache.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apache\_setenv()**для установки переменной окружения Apache.**

```php
<?php
apache_setenv("EXAMPLE_VAR", "Какое-либо значение");
?>
```

### Примітки

> **Зауваження** :
> 
> **apache\_setenv()** можна використовувати разом з [apache\_getenv()](function.apache-getenv.md) на різних сторінках або для визначення змінних, які потрібно передати увімкненням на стороні сервера SSI (.shtml), які, у свою чергу, були включені в PHP-скрипти.

### Дивіться також

-   [apache\_getenv()](function.apache-getenv.md) \- Повертає змінну оточення підпроцесу сервера Apache

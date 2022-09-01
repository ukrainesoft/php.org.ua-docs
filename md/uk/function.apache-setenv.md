---
navigation:
  - function.apache-response-headers.html: « apacheresponseheaders
  - function.getallheaders.md: getallheaders »
  - index.md: PHP Manual
  - ref.apache.md: Функции Apache
title: apachesetenv
---
# apachesetenv

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

apachesetenv - Встановлює змінну subprocessenv Apache

### Опис

```methodsynopsis
apache_setenv(string $variable, string $value, bool $walk_to_top = false): bool
```

**apachesetenv()** встановлює значення змінної оточення Apache, визначеної як `variable`

> **Зауваження**
> 
> При установці змінної оточення Apache, відповідна їй змінна [SERVER](reserved.variables.server.md) не змінюється.

### Список параметрів

`variable`

Змінне оточення, яке потрібно встановити.

`value`

Нове значення змінної `variable`

`walk_to_top`

Чи робити доступною змінну для всіх рівнів Apache.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apachesetenv()** для встановлення змінного оточення Apache.**

```php
<?php
apache_setenv("EXAMPLE_VAR", "Какое-либо значение");
?>
```

### Примітки

> **Зауваження**
> 
> **apachesetenv()** можна використовувати разом з [apachegetenv()](function.apache-getenv.md) на різних сторінках або визначення змінних, які потрібно передати включенням на стороні сервера SSI (.shtml), які, у свою чергу, були включені в PHP-скрипти.

### Дивіться також

-   [apachegetenv()](function.apache-getenv.md) - Повертає змінну оточення підпроцесу сервера Apache

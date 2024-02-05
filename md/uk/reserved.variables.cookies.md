---
navigation:
  - reserved.variables.environment.md: « $\_ENV
  - reserved.variables.phperrormsg.md: $php\_errormsg »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_COOKIE
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_COOKIE

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_COOKIE — HTTP Cookies

### Опис

Асоціативний масив (array) значень переданих скрипту через HTTP Cookies.

### Приклади

**Приклад #1 Приклад використання $\_COOKIE**

```php
<?php
echo 'Привет, ' . htmlspecialchars($_COOKIE["name"]) . '!';
?>
```

Припустимо, що значення cookie з ім'ям "name" було встановлено раніше.

Висновок наведеного прикладу буде схожим на:

```
Привет, Иван!
```

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [setcookie()](function.setcookie.md) \- Надсилає cookie
-   [Обробка зовнішніх змінних](language.variables.external.md)
-   [Фільтрування даних](book.filter.md)

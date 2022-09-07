---
navigation:
  - reserved.variables.environment.md: ENV
  - reserved.variables.phperrormsg.md: $phperrormsg »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: COOKIE
---
# COOKIE

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

COOKIE - HTTP Cookies

### Опис

Асоціативний масив (array) значень переданих скрипту через HTTP Cookies.

### Приклади

**Приклад #1 Приклад використання $COOKIE**

```php
<?php
echo 'Привет, ' . htmlspecialchars($_COOKIE["name"]) . '!';
?>
```

Припустимо, що значення cookie з ім'ям "name" було встановлено раніше.

Результатом виконання цього прикладу буде щось подібне:

```
Привет, Иван!
```

### Примітки

> **Зауваження**
> 
> Це 'суперглобальна' або автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [setcookie()](function.setcookie.md) - Надсилає cookie
-   [Обробка зовнішніх змінних](language.variables.external.md)
-   [Фільтрування даних](book.filter.md)

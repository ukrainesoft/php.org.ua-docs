HTTP Cookies

-   [ENV](reserved.variables.environment.html)
    
-   [$phperrormsg »](reserved.variables.phperrormsg.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   HTTP Cookies
    

# COOKIE

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

COOKIE - HTTP Cookies

### Опис

Асоціативний масив (array) значень переданих скрипту через HTTP Cookies.

### Приклади

**Приклад #1 Приклад використання $COOKIE**

```php
<?php
echo 'Привет, ' . htmlspecialchars($_COOKIE["name"]) . '!';
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

-   [setcookie()](function.setcookie.html) - Надсилає cookie
-   [Обработка внешних переменных](language.variables.external.html)
-   [Фільтрування даних](book.filter.html)
---
navigation:
  - function.restore-error-handler.md: « restore\_error\_handler
  - function.set-error-handler.md: set\_error\_handler »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: restore\_exception\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# restore\_exception\_handler

(PHP 5, PHP 7, PHP 8)

restore\_exception\_handler — Відновлює попередній обробник винятків

### Опис

```methodsynopsis
restore_exception_handler(): true
```

Використовується після зміни обробника виключень функцією [set\_exception\_handler()](function.set-exception-handler.md), щоб повернути попередній обробник (який може бути як вбудованою функцією, так і певною користувачем).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Пример #1 Пример использования**restore\_exception\_handler()\*\*\*\*

```php
<?php
    function exception_handler_1(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    function exception_handler_2(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    set_exception_handler('exception_handler_1');
    set_exception_handler('exception_handler_2');

    restore_exception_handler();

    throw new Exception('Вызван первый обработчик исключений...');
?>
```

Результат виконання наведеного прикладу:

```
[exception_handler_1] Вызван первый обработчик исключений...
```

### Дивіться також

-   [set\_exception\_handler()](function.set-exception-handler.md) \- Задає користувальницький обробник винятків
-   [set\_error\_handler()](function.set-error-handler.md) \- Задає користувальницький обробник помилок
-   [restore\_error\_handler()](function.restore-error-handler.md) \- Відновлює попередній обробник помилок
-   [error\_reporting()](function.error-reporting.md) \- Встановлює, які помилки PHP потраплять у звіт

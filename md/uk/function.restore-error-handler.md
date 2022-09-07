---
navigation:
  - function.error-reporting.md: « errorreporting
  - function.restore-exception-handler.md: restoreexceptionhandler »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: restoreerrorhandler
---
# restoreerrorhandler

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

restoreerrorhandler — Відновлює попередній обробник помилок

### Опис

```methodsynopsis
restore_error_handler(): bool
```

Використовується після зміни обробника помилок функцією [seterrorhandler()](function.set-error-handler.md), щоб повернути попередній обробник (який може бути як вбудованою функцією, так і певною користувачем).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ця функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **restoreerrorhandler()****

Визначення, чи сталася помилка у функції [unserialize()](function.unserialize.md), а потім відновлення вихідного обробника помилок.

```php
<?php
function unserialize_handler($errno, $errstr)
{
    echo "Сериализуемое значение недопустимо.\n";
}

$serialized = 'foo';
set_error_handler('unserialize_handler');
$original = unserialize($serialized);
restore_error_handler();
?>
```

Результат виконання цього прикладу:

```
Сериализуемое значение недопустимо.
```

### Дивіться також

-   [errorreporting()](function.error-reporting.md) - Задає, які помилки PHP потраплять у звіт
-   [seterrorhandler()](function.set-error-handler.md) - Задає користувальницький обробник помилок
-   [restoreexceptionhandler()](function.restore-exception-handler.md) - Відновлює попередній обробник винятків
-   [triggererror()](function.trigger-error.md) - Викликає помилку користувача/попередження/повідомлення

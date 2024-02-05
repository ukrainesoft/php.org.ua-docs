---
navigation:
  - function.error-reporting.md: « error\_reporting
  - function.restore-exception-handler.md: restore\_exception\_handler »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: restore\_error\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# restore\_error\_handler

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

restore\_error\_handler — Відновлює попередній обробник помилок

### Опис

```methodsynopsis
restore_error_handler(): true
```

Використовується після зміни обробника помилок функцією [set\_error\_handler()](function.set-error-handler.md), щоб повернути попередній обробник (який може бути як вбудованою функцією, так і певною користувачем).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Пример #1 Пример использования**restore\_error\_handler()\*\*\*\*

Определение, произошла ли ошибка в функции[unserialize()](function.unserialize.md), а потім відновлення вихідного обробника помилок.

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

Результат виконання наведеного прикладу:

```
Сериализуемое значение недопустимо.
```

### Дивіться також

-   [error\_reporting()](function.error-reporting.md) \- Встановлює, які помилки PHP потраплять у звіт
-   [set\_error\_handler()](function.set-error-handler.md) \- Задає користувальницький обробник помилок
-   [restore\_exception\_handler()](function.restore-exception-handler.md) \- Відновлює попередній обробник винятків
-   [trigger\_error()](function.trigger-error.md) \- Викликає помилку користувача/попередження/повідомлення

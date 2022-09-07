---
navigation:
  - function.set-exception-handler.md: « setexceptionhandler
  - function.user-error.md: usererror »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: triggererror
---
# triggererror

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

triggererror — Викликає помилку користувача/попередження/сповіщення

### Опис

```methodsynopsis
trigger_error(string $message, int $error_level = E_USER_NOTICE): bool
```

Використовується для виклику помилок користувача. Можна використовувати у зв'язці з вбудованим обробником помилок, а також з обробником користувача, заданим функцією [seterrorhandler()](function.set-error-handler.md)

Ця функція може бути корисною, якщо потрібно згенерувати певну реакцію на виняток під час виконання.

### Список параметрів

`message`

Повідомлення, що відповідає цій помилці. Обмежено 1024 байтами завдовжки. Символи далі 1024 будуть обрізані.

`error_level`

Визначений тип помилки. Працює тільки з сімейством констант EUSER. За замовчуванням **`E_USER_NOTICE`**

### Значення, що повертаються

Функція повертає \*\*`false`\*\*якщо заданий неправильний `error_level`, і **`true`** в інших випадках.

### Приклади

**Приклад #1 Приклад використання **triggererror()****

Докладніший приклад наведено в описі функції [seterrorhandler()](function.set-error-handler.md)

```php
<?php
if ($divisor == 0) {
    trigger_error("Не могу поделить на ноль", E_USER_ERROR);
}
?>
```

### Примітки

**Увага**

HTML-сутності в `message` не екрановані. Щоб відобразити повідомлення у браузері, перетворіть його функцією [htmlentities()](function.htmlentities.md)

### Дивіться також

-   [errorreporting()](function.error-reporting.md) - Задає, які помилки PHP потраплять у звіт
-   [seterrorhandler()](function.set-error-handler.md) - Задає користувальницький обробник помилок
-   [restoreerrorhandler()](function.restore-error-handler.md) - Відновлює попередній обробник помилок
-   [Константи рівнів помилок](errorfunc.constants.md)

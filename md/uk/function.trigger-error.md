---
navigation:
  - function.set-exception-handler.md: « set\_exception\_handler
  - function.user-error.md: user\_error »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: trigger\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trigger\_error

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

trigger\_error — Викликає помилку користувача/попередження/сповіщення

### Опис

```methodsynopsis
trigger_error(string $message, int $error_level = E_USER_NOTICE): bool
```

Використовується для виклику помилок користувача. Можна використовувати у зв'язці з вбудованим обробником помилок, а також з обробником користувача, заданим функцією [set\_error\_handler()](function.set-error-handler.md)

Ця функція може бути корисною, якщо потрібно згенерувати певну реакцію на виняток під час виконання.

### Список параметрів

`message`

Повідомлення, що відповідає цій помилці. Обмежено 1024 байтами завдовжки. Символи далі 1024 будуть обрізані.

`error_level`

Визначений тип помилки. Працює тільки з сімейством констант E\_USER. По умолчанию\*\*`E_USER_NOTICE`\*\*

### Значення, що повертаються

Функція повертає **`false`**якщо заданий неправильний `error_level`, и**`true`** в інших випадках.

### Приклади

**Пример #1 Пример использования**trigger\_error()\*\*\*\*

Більш детальний приклад наведено в описі функції [set\_error\_handler()](function.set-error-handler.md)

```php
<?php
if ($divisor == 0) {
    trigger_error("Не могу поделить на ноль", E_USER_ERROR);
}
?>
```

### Примітки

**Увага**

HTML-сутності в `message` не екрановані. Щоб відобразити повідомлення у браузері, перетворіть його функцією [htmlentities()](function.mdentities.md)

### Дивіться також

-   [error\_reporting()](function.error-reporting.md) \- Встановлює, які помилки PHP потраплять у звіт
-   [set\_error\_handler()](function.set-error-handler.md) \- Задає користувальницький обробник помилок
-   [restore\_error\_handler()](function.restore-error-handler.md) \- Відновлює попередній обробник помилок
-   [Константи рівнів помилок](errorfunc.constants.md)

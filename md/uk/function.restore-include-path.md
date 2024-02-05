---
navigation:
  - function.putenv.md: « putenv
  - function.set-include-path.md: set\_include\_path »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: restore\_include\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# restore\_include\_path

(PHP 4 >= 4.3.0, PHP 5, PHP 7)

restore\_include\_path — Відновлює початкове значення конфігураційної установки include\_path

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
restore_include_path(): void
```

Відновлює вихідне значення конфігураційної установки [include\_path](ini.core.md#ini.include-path), яка записана в php.ini

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**restore\_include\_path()\*\*\*\*

```php
<?php

echo get_include_path();  // .:/usr/local/lib/php

set_include_path('/inc');

echo get_include_path();  // /inc

restore_include_path();

// или так
ini_restore('include_path');

echo get_include_path();  // .:/usr/local/lib/php

?>
```

### Дивіться також

-   [ini\_restore()](function.ini-restore.md) \- Відновлює налаштування конфігурації.
-   [get\_include\_path()](function.get-include-path.md) \- Отримання поточного значення конфігураційної установки include\_path
-   [set\_include\_path()](function.set-include-path.md) \- Встановлює налаштування конфігурації include\_path
-   [include](function.include.md) \- include

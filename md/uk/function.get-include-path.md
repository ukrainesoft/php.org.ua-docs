---
navigation:
  - function.get-extension-funcs.md: « getextensionfuncs
  - function.get-included-files.md: getincludedfiles »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getincludepath
---
# getincludepath

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

getincludepath — Отримання поточного значення конфігураційної установки includepath

### Опис

```methodsynopsis
get_include_path(): string|false
```

Отримує значення налаштування конфігурації [includepath](ini.core.md#ini.include-path)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу у вигляді рядка або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **getincludepath()****

```php
<?php
echo get_include_path();

// или используя ini_get()
echo ini_get('include_path');
?>
```

### Дивіться також

-   [iniget()](function.ini-get.md) - Отримує значення налаштування конфігурації
-   [restoreincludepath()](function.restore-include-path.md) - Відновлює початкове значення конфігураційної установки includepath
-   [setincludepath()](function.set-include-path.md) - Встановлює налаштування конфігурації includepath
-   [include](function.include.md) - include

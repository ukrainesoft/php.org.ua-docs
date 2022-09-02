---
navigation:
  - function.restore-include-path.md: « restoreincludepath
  - function.set-time-limit.md: settimelimit »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: setincludepath
---
# setincludepath

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

setincludepath — Встановлює налаштування конфігурації includepath

### Опис

```methodsynopsis
set_include_path(string $include_path): string|false
```

Задає значення конфігураційної установки [includepath](ini.core.md#ini.include-path) тимчасово виконання скрипта.

### Список параметрів

`include_path`

Нове значення налаштування [includepath](ini.core.md#ini.include-path)

### Значення, що повертаються

Повертає старе значення [includepath](ini.core.md#ini.include-path) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **setincludepath()****

```php
<?php
set_include_path('/usr/lib/pear');

// Или так
ini_set('include_path', '/usr/lib/pear');
?>
```

**Приклад #2 Упорядкування більш довгого шляху include path**

Використовуючи константу **`PATH_SEPARATOR`**, можна додати до шляху вкладені директорії незалежно від операційної системи.

У цьому прикладі ми додамо /usr/lib/pear до кінця існуючого шляху `include_path`

```php
<?php
$path = '/usr/lib/pear';
set_include_path(get_include_path() . PATH_SEPARATOR . $path);
?>
```

### Дивіться також

-   [iniset()](function.ini-set.md) - Встановлює налаштування конфігурації
-   [getincludepath()](function.get-include-path.md) - Отримання поточного значення конфігураційної установки includepath
-   [restoreincludepath()](function.restore-include-path.md) - Відновлює початкове значення конфігураційної установки includepath
-   [include](function.include.md) - include

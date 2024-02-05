---
navigation:
  - function.restore-include-path.md: « restore\_include\_path
  - function.set-time-limit.md: set\_time\_limit »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: set\_include\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# set\_include\_path

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

set\_include\_path — Встановлює налаштування конфігурації include\_path

### Опис

```methodsynopsis
set_include_path(string $include_path): string|false
```

Задає значення конфігураційної установки [include\_path](ini.core.md#ini.include-path) тимчасово виконання скрипта.

### Список параметрів

`include_path`

Новое значение настройки[include\_path](ini.core.md#ini.include-path)

### Значення, що повертаються

Возвращает старое значение[include\_path](ini.core.md#ini.include-path) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** set\_include\_path()\*\*\*\*

```php
<?php
set_include_path('/usr/lib/pear');

// Или так
ini_set('include_path', '/usr/lib/pear');
?>
```

**Приклад #2 Упорядкування більш довгого шляху include path**

Используя константу\*\*`PATH_SEPARATOR`\*\*, можна додати до шляху вкладені директорії незалежно від операційної системи.

У цьому прикладі ми додамо /usr/lib/pear до кінця існуючого шляху `include_path`

```php
<?php
$path = '/usr/lib/pear';
set_include_path(get_include_path() . PATH_SEPARATOR . $path);
?>
```

### Дивіться також

-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації
-   [get\_include\_path()](function.get-include-path.md) \- Отримання поточного значення конфігураційної установки include\_path
-   [restore\_include\_path()](function.restore-include-path.md) \- Відновлює початкове значення конфігураційної установки include\_path
-   [include](function.include.md) \- include

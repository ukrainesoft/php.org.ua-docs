---
navigation:
  - function.get-extension-funcs.md: « get\_extension\_funcs
  - function.get-included-files.md: get\_included\_files »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_include\_path
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_include\_path

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

get\_include\_path — Отримання поточного значення конфігураційної установки include\_path

### Опис

```methodsynopsis
get_include_path(): string|false
```

Отримує значення налаштування конфігурації [include\_path](ini.core.md#ini.include-path)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**get\_include\_path()\*\*\*\*

```php
<?php
echo get_include_path();

// или используя ini_get()
echo ini_get('include_path');
?>
```

### Дивіться також

-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [restore\_include\_path()](function.restore-include-path.md) \- Відновлює початкове значення конфігураційної установки include\_path
-   [set\_include\_path()](function.set-include-path.md) \- Встановлює налаштування конфігурації include\_path
-   [include](function.include.md) \- include

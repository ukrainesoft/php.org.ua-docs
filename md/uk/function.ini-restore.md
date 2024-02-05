---
navigation:
  - function.ini-parse-quantity.md: « ini\_parse\_quantity
  - function.ini-set.md: ini\_set »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: ini\_restore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ini\_restore

(PHP 4, PHP 5, PHP 7, PHP 8)

ini\_restore — Відновлює налаштування конфігурації.

### Опис

```methodsynopsis
ini_restore(string $option): void
```

Відновлює початкове значення конфігураційної установки.

### Список параметрів

`option`

Ім'я налаштування.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ini\_restore()\*\*\*\*

```php
<?php
$setting = 'html_errors';

echo 'Текущее значение настройки \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;

ini_set($setting, ini_get($setting) ? 0 : 1);
echo 'Новое значение настройки \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;

ini_restore($setting);
echo 'Исходное значение настройки \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;
?>
```

Результат виконання наведеного прикладу:

```
Текущее значение настройки 'html_errors': 1
Новое значение настройки 'html_errors': 0
Исходное значение настройки 'html_errors': 1
```

### Дивіться також

-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [ini\_get\_all()](function.ini-get-all.md) \- Отримує всі налаштування конфігурації
-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації

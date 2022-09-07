---
navigation:
  - function.ini-get.md: « iniget
  - function.ini-set.md: iniset »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: inirestore
---
# inirestore

(PHP 4, PHP 5, PHP 7, PHP 8)

inirestore — Відновлює налаштування конфігурації.

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

**Приклад #1 Приклад використання **inirestore()****

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

Результат виконання цього прикладу:

```
Текущее значение настройки 'html_errors': 1
Новое значение настройки 'html_errors': 0
Исходное значение настройки 'html_errors': 1
```

### Дивіться також

-   [iniget()](function.ini-get.md) - Отримує значення налаштування конфігурації
-   [inigetall()](function.ini-get-all.md) - Отримує всі налаштування конфігурації
-   [iniset()](function.ini-set.md) - Встановлює налаштування конфігурації

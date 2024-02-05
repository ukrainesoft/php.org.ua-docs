---
navigation:
  - function.ini-get-all.md: « ini\_get\_all
  - function.ini-parse-quantity.md: ini\_parse\_quantity »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: ini\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ini\_get

(PHP 4, PHP 5, PHP 7, PHP 8)

ini\_get — Отримує значення конфігураційної установки

### Опис

```methodsynopsis
ini_get(string $option): string|false
```

У разі успішного виконання повертає значення конфігураційної установки.

### Список параметрів

`option`

Ім'я конфігураційної установки.

### Значення, що повертаються

Повертає значення конфігурації у вигляді рядка. Для значень `null` повертатиметься порожній рядок. Функція поверне **`false`**, якщо вказане налаштування не існує.

### Приклади

**Приклад #1 Декілька прикладів використання **ini\_get()****

```php
<?php
/*
Наш файл php.ini содержит следующие настройки:

display_errors = On
register_globals = Off
post_max_size = 8M
*/

echo 'display_errors = ' . ini_get('display_errors') . "\n";
echo 'register_globals = ' . ini_get('register_globals') . "\n";
echo 'post_max_size = ' . ini_get('post_max_size') . "\n";
echo 'post_max_size+1 = ' . (ini_get('post_max_size')+1) . "\n";
echo 'post_max_size in bytes = ' . return_bytes(ini_get('post_max_size'));

function return_bytes($val) {
    $val = trim($val);
    $last = strtolower($val[strlen($val)-1]);
    switch($last) {
        // Модификатор 'G' доступен
        case 'g':
            $val *= 1024;
        case 'm':
            $val *= 1024;
        case 'k':
            $val *= 1024;
    }

    return $val;
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
display_errors = 1
register_globals = 0
post_max_size = 8M
post_max_size+1 = 9
post_max_size in bytes = 8388608
```

### Примітки

> **Зауваження** **Логічні значення, що повертаються**
> 
> Boolean-значение ini-настройки`off` буде повернено у вигляді порожнього рядка або рядка "0", тоді як значення `on` відповідатиме рядок "1". Функція також може повертати буквені значення налаштування INI.

> **Зауваження** **Значення кількості пам'яті, що повертаються**
> 
> Багато ini-налаштувань, значення яких вимірюються кількістю пам'яті, такі як [upload\_max\_filesize](ini.core.md#ini.upload-max-filesize), зберігаються у php.ini у скороченому вигляді . **ini\_get()** поверне саме те, що записано у файлі php.ini, а *НЕ* цілий (int) еквівалент цієї величини. Спроба використання отриманої величини в арифметичних операціях не дасть бажаного результату. У наведеному вище прикладі продемонстровано, як можна перевести скорочений запис до числа байт.

> **Зауваження** :
> 
> **ini\_get()** не може прочитати параметри типу "масив", такі як pdo.dsn.\*, і повертає \*\*`false`\*\*таких случаях.

### Дивіться також

-   [get\_cfg\_var()](function.get-cfg-var.md) \- Витягує значення налаштування конфігурації PHP
-   [ini\_get\_all()](function.ini-get-all.md) \- Отримує всі налаштування конфігурації
-   [ini\_restore()](function.ini-restore.md) \- Відновлює налаштування конфігурації.
-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації

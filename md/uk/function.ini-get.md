Отримує значення налаштування конфігурації

-   [« inigetall](function.ini-get-all.html)
    
-   [inirestore »](function.ini-restore.html)
    
-   [PHP Manual](index.md)
    
-   [Опції PHP/інформаційні функції](ref.info.md)
    
-   Отримує значення налаштування конфігурації
    

# iniget

(PHP 4, PHP 5, PHP 7, PHP 8)

iniget — Отримує значення конфігураційної установки

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

**Приклад #1 Декілька прикладів використання **iniget()****

```php
<?php
/*
Наш файл php.ini содержит следующие настройки:

display_errors = On
register_globals = Off
post_max_size = 8M
*/

echo 'display_errors = ' . ini_get('display_errors') . "\n";
echo 'register_globals = ' . ini_get('register_globals') . "\n";
echo 'post_max_size = ' . ini_get('post_max_size') . "\n";
echo 'post_max_size+1 = ' . (ini_get('post_max_size')+1) . "\n";
echo 'post_max_size in bytes = ' . return_bytes(ini_get('post_max_size'));

function return_bytes($val) {
    $val = trim($val);
    $last = strtolower($val[strlen($val)-1]);
    switch($last) {
        // Модификатор 'G' доступен
        case 'g':
            $val *= 1024;
        case 'm':
            $val *= 1024;
        case 'k':
            $val *= 1024;
    }

    return $val;
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

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
> Boolean-значення ini-налаштування `off` буде повернено у вигляді порожнього рядка або рядка "0", тоді як значення `on` відповідатиме рядок "1". Функція також може повертати буквені значення налаштування INI.

> **Зауваження** **Значення кількості пам'яті, що повертаються.**
> 
> Багато ini-налаштувань, значення яких вимірюються кількістю пам'яті, такі як [uploadmaxfilesize](ini.core.html#ini.upload-max-filesize), зберігаються у php.ini у скороченому вигляді . **iniget()** поверне саме те, що записано у файлі php.ini, а *НЕ* цілий (int) еквівалент цієї величини. Спроба використання отриманої величини в арифметичних операціях не дасть бажаного результату. У наведеному вище прикладі продемонстровано, як можна перевести скорочений запис до числа байт.

> **Зауваження**
> 
> **iniget()** не може прочитати параметри типу "масив", такі як pdo.dsn., і повертає **`false`** таких випадках.

### Дивіться також

-   [getcfgvar()](function.get-cfg-var.html) - Витягує значення налаштування конфігурації PHP
-   [inigetall()](function.ini-get-all.html) - Отримує всі налаштування конфігурації
-   [inirestore()](function.ini-restore.html) - Відновлює налаштування конфігурації.
-   [iniset()](function.ini-set.html) - Встановлює налаштування конфігурації
---
navigation:
  - function.parse-ini-file.md: « parse\_ini\_file
  - function.pathinfo.md: pathinfo »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: parse\_ini\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parse\_ini\_string

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

parse\_ini\_string — Розбирає рядок конфігурації

### Опис

```methodsynopsis
parse_ini_string(string $ini_string, bool $process_sections = false, int $scanner_mode = INI_SCANNER_NORMAL): array|false
```

**parse\_ini\_string()** повертає налаштування з рядка `ini_string` у вигляді асоціативного масиву.

Структура INI-рядка така сама, як і в php.ini.

### Список параметрів

`ini_string`

Вміст INI-файлу, що розбирається.

`process_sections`

Установив в параметр`process_sections` **`true`**, можна отримати багатовимірний масив, який включає назви секцій та налаштувань. За замовчуванням `process_sections`равен\*\*`false`\*\*

`scanner_mode`

Може приймати такі значення: **`INI_SCANNER_NORMAL`**(по умолчанию) или\*\*`INI_SCANNER_RAW`**Если указано значение**`INI_SCANNER_RAW`\*\*то значення опцій не будуть оброблятися.

З версії PHP 5.6.1 можна також задати **`INI_SCANNER_TYPED`**. У цьому режимі типи boolean, null і integer, по можливості, зберігатимуться. Строкові значення `"true"` `"on"`и`"yes"` будуть перетворені на **`true`**. . `"false"` `"off"` `"no"`и`"none"`в\*\*`false`\*\*. . `"null"` перетворюється на **`null`**. Крім цього, усі числові рядки будуть, по можливості, перетворені до цілих чисел.

### Значення, що повертаються

У разі успішного виконання налаштування повертаються у вигляді асоціативного масиву (array). У разі виникнення помилки повертається **`false`**

### Примітки

> **Зауваження**: Існує зарезервовані слова, які не можна використовувати як ключі в ini-файлах. Такими словами є: `null` `yes` `no` `true` `false` `on` `off` `none`Значения`null` `off` `no`и`false`преобразуются в`""`, а значения`on` `yes`и`true`в`"1"` , але тільки якщо не використовується режим **`INI_SCANNER_TYPED`** (Доступний з PHP 5.6.1). Символи `?{}|&~!()^"` не повинні використовуватися в ключах і мати будь-який особливий зміст у значеннях.

### Дивіться також

-   [parse\_ini\_file()](function.parse-ini-file.md) \- Обробляє конфігураційний файл

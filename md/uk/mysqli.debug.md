---
navigation:
  - mysqli.construct.md: '« mysqli::\_\_construct'
  - mysqli.dump-debug-info.md: 'mysqli::dump\_debug\_info »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::debug'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::debug

# mysqli\_debug

(PHP 5, PHP 7, PHP 8)

mysqli::debug -- mysqli\_debug — Виконує процедури налагодження

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::debug(string $options): true
```

Процедурний стиль

```methodsynopsis
mysqli_debug(string $options): true
```

Виконує процедури налагодження за допомогою бібліотеки Fred Fish.

### Список параметрів

`options`

Рядок, що містить процедуру налагодження, що виконується.

Рядок управління налагодженням - це послідовність полів, розділених двокрапками, як показано нижче:

```
<field_1>:<field_2>:<field_N>
```

Кожне поле складається з обов'язкового символу прапора, за яким слідує необов'язковий символ `,` і список модифікаторів, розділений комами: `flag[,modifier,modifier,...,modifier]`

**Допустимі символи прапорів**

| Символ `options` | Опис |
| --- | --- |
| O | **`MYSQLND_DEBUG_FLUSH`** |
| A/a | **`MYSQLND_DEBUG_APPEND`** |
| F | **`MYSQLND_DEBUG_DUMP_FILE`** |
| i | **`MYSQLND_DEBUG_DUMP_PID`** |
| L | **`MYSQLND_DEBUG_DUMP_LINE`** |
| m | **`MYSQLND_DEBUG_TRACE_MEMORY_CALLS`** |
| n | **`MYSQLND_DEBUG_DUMP_LEVEL`** |
| o | виведення у файл |
| T | **`MYSQLND_DEBUG_DUMP_TIME`** |
| t | **`MYSQLND_DEBUG_DUMP_TRACE`** |
| x | **`MYSQLND_DEBUG_PROFILE_CALLS`** |

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер повертає значення **`true`**. . Раніше вона повертала значення \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Генерація файлу трасування**

```php
<?php

/* Создать файл трассировки в '/tmp/client.trace' на локальной машине (клиенте): */
mysqli_debug("d:t:o,/tmp/client.trace");

?>
```

### Примітки

> **Зауваження** :
> 
> Щоб функція **mysqli\_debug()** була доступна, необхідно скомпілювати клієнтську бібліотеку MySQL за допомогою налагодження.

### Дивіться також

-   [mysqli\_dump\_debug\_info()](mysqli.dump-debug-info.md) \- Журналування налагоджувальної інформації
-   [mysqli\_report()](function.mysqli-report.md) \- Псевдонім mysqli\_driver->report\_mode

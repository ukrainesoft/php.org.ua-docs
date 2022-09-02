---
navigation:
  - mysqli.construct.md: '« mysqli::construct'
  - mysqli.dump-debug-info.md: 'mysqli::dumpdebuginfo »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::debug'
---
# mysqli::debug

# mysqlidebug

(PHP 5, PHP 7, PHP 8)

mysqli::debug -- mysqlidebug — Виконує процедури налагодження

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::debug(string $options): bool
```

Процедурний стиль

```methodsynopsis
mysqli_debug(string $options): bool
```

Виконує процедури налагодження за допомогою бібліотеки Fred Fish.

### Список параметрів

`options`

Рядок, що містить процедуру налагодження, що виконується.

Рядок управління налагодженням є послідовністю полів, розділених двокрапками, як показано нижче:

```
<field_1>:<field_2>:<field_N>
```

. Кожне поле складається з обов'язкового символу прапора, за яким слідує необов'язковий символ `,` і список модифікаторів, розділений комами: `flag[,modifier,modifier,...,modifier]`

**Допустимі символи прапорів**

| Символ `option` | Описание |
| --- | --- |
| Про | **`MYSQLND_DEBUG_FLUSH`** |
| A/a | **`MYSQLND_DEBUG_APPEND`** |
| Ф | **`MYSQLND_DEBUG_DUMP_FILE`** |
| і | **`MYSQLND_DEBUG_DUMP_PID`** |
| Л | **`MYSQLND_DEBUG_DUMP_LINE`** |
| м | **`MYSQLND_DEBUG_TRACE_MEMORY_CALLS`** |
| н | **`MYSQLND_DEBUG_DUMP_LEVEL`** |
| про | виведення у файл |
| Т | **`MYSQLND_DEBUG_DUMP_TIME`** |
| т | **`MYSQLND_DEBUG_DUMP_TRACE`** |
| з | **`MYSQLND_DEBUG_PROFILE_CALLS`** |

### Значення, що повертаються

Повертає **`true`**

### Приклади

**Приклад #1 Генерація файлу трасування**

```php
<?php

/* Создать файл трассировки в '/tmp/client.trace' на локальной машине (клиенте): */
mysqli_debug("d:t:o,/tmp/client.trace");

?>
```

### Примітки

> **Зауваження**
> 
> Щоб використовувати функцію **mysqlidebug()** вам потрібно скомпілювати клієнтську бібліотеку MySQL за допомогою налагодження.

### Дивіться також

-   [mysqlidumpdebuginfo()](mysqli.dump-debug-info.md) - Журналування налагоджувальної інформації
-   [mysqlireport()](function.mysqli-report.md) - Псевдонім mysqlidriver->reportmode

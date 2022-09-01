---
navigation:
  - function.get-browser.html: « getbrowser
  - function.highlight-file.html: highlightfile »
  - index.html: PHP Manual
  - ref.misc.html: Різні функції
title: haltcompiler
---
# haltcompiler

(PHP 5> = 5.1.0, PHP 7, PHP 8)

haltcompiler — Зупиняє роботу компілятора

### Опис

```methodsynopsis
__halt_compiler(): void
```

Зупиняє роботу компілятора. Ця функція може бути корисною при введенні даних у PHP-скрипти, наприклад, у файли установки.

Початкова позиція даних у байтах може бути визначена константою **`__COMPILER_HALT_OFFSET__`**, яка може бути визначена, тільки якщо у файлі є функція **haltcompiler()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **haltcompiler()****

```php
<?php

// открыть указанный файл
$fp = fopen(__FILE__, 'r');

// искать в указателе файла данные
fseek($fp, __COMPILER_HALT_OFFSET__);

// и вывести их
var_dump(stream_get_contents($fp));

// останавливает работу скрипта
__halt_compiler(); the installation data (eg. tar, gz, PHP, etc.)
```

### Примітки

> **Зауваження**
> 
> Функція **haltcompiler()** може бути використана лише ззовні.

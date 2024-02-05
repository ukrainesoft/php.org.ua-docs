---
navigation:
  - function.get-browser.md: « get\_browser
  - function.highlight-file.md: highlight\_file »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: \_\_halt\_compiler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# \_\_halt\_compiler

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

\_\_halt\_compiler — Зупиняє роботу компілятора

### Опис

```methodsynopsis
__halt_compiler(): void
```

Зупиняє роботу компілятора. Ця функція може бути корисною при введенні даних у PHP-скрипти, наприклад, у файли установки.

Початкова позиція даних у байтах може бути визначена константою **`__COMPILER_HALT_OFFSET__`**, яка може бути визначена, тільки якщо у файлі є функція **\_\_halt\_compiler()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**\_\_halt\_compiler()\*\*\*\*

```php
<?php

// открыть указанный файл
$fp = fopen(__FILE__, 'r');

// искать в указателе файла данные
fseek($fp, __COMPILER_HALT_OFFSET__);

// и вывести их
var_dump(stream_get_contents($fp));

// останавливает работу скрипта
__halt_compiler(); the installation data (eg. tar, gz, PHP, etc.)
```

### Примітки

> **Зауваження** :
> 
> Функция**\_\_halt\_compiler()** може бути використана лише ззовні.

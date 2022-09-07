---
navigation:
  - function.get-include-path.md: « getincludepath
  - function.get-loaded-extensions.md: getloadedextensions »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getincludedfiles
---
# getincludedfiles

(PHP 4, PHP 5, PHP 7, PHP 8)

getincludedfiles — Повертає масив імен увімкнених у скрипт файлів

### Опис

```methodsynopsis
get_included_files(): array
```

Отримує імена всіх файлів, які були включені до скрипту з використанням [include](function.include.md) [includeonce](function.include-once.md) [require](function.require.md) або [requireonce](function.require-once.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, який містить імена всіх файлів.

Скрипт, який був завантажений спочатку, розглядається як "включений файл", тому він також потрапить до списку файлів, включених функцією [include](function.include.md) чи іншими.

Файли, що додаються в скрипт неодноразово, потраплять до масиву лише в одному екземплярі.

### Приклади

**Приклад #1 Приклад використання **getincludedfiles()****

```php
<?php
// Этот скрипт расположен в файле abc.php

include 'test1.php';
include_once 'test2.php';
require 'test3.php';
require_once 'test4.php';

$included_files = get_included_files();

foreach ($included_files as $filename) {
    echo "$filename\n";
}

?>
```

Результат виконання цього прикладу:

```
/path/to/abc.php
/path/to/test1.php
/path/to/test2.php
/path/to/test3.php
/path/to/test4.php
```

### Дивіться також

-   [include](function.include.md) - include
-   [includeonce](function.include-once.md) - includeonce
-   [require](function.require.md) - require
-   [requireonce](function.require-once.md) - requireonce
-   [getrequiredfiles()](function.get-required-files.md) - Псевдонім getincludedfiles

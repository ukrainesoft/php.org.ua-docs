---
navigation:
  - function.get-include-path.md: « get\_include\_path
  - function.get-loaded-extensions.md: get\_loaded\_extensions »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_included\_files
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_included\_files

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_included\_files — Повертає масив імен увімкнених у скрипт файлів

### Опис

```methodsynopsis
get_included_files(): array
```

Отримує імена всіх файлів, які були включені до скрипту з використанням [include](function.include.md) [include\_once](function.include-once.md) [require](function.require.md) або [require\_once](function.require-once.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, який містить імена всіх файлів.

Скрипт, який був завантажений спочатку, розглядається як "включений файл", тому він також потрапить до списку файлів, включених функцією [include](function.include.md)или другими.

Файли, що додаються в скрипт неодноразово, потраплять до масиву лише в одному екземплярі.

### Приклади

**Пример #1 Пример использования**get\_included\_files()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
/path/to/abc.php
/path/to/test1.php
/path/to/test2.php
/path/to/test3.php
/path/to/test4.php
```

### Дивіться також

-   [include](function.include.md) \- include
-   [include\_once](function.include-once.md) \- include\_once
-   [require](function.require.md) \- require
-   [require\_once](function.require-once.md) \- require\_once
-   [get\_required\_files()](function.get-required-files.md) \- Псевдонім get\_included\_files

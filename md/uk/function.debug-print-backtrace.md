---
navigation:
  - function.debug-backtrace.md: « debug\_backtrace
  - function.error-clear-last.md: error\_clear\_last »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: debug\_print\_backtrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# debug\_print\_backtrace

(PHP 5, PHP 7, PHP 8)

debug\_print\_backtrace — Виводить стек викликів функцій

### Опис

```methodsynopsis
debug_print_backtrace(int $options = 0, int $limit = 0): void
```

**debug\_print\_backtrace()** виводить стек викликів функцій. Виводить дзвінки функцій, імена включених/потрібних файлів та іншу інформацію з функцій ([eval()](function.eval.md)

### Список параметрів

`options`

Аргумент є бітовою маскою для наступних налаштувань:

<table class="doctable table"><caption><strong>Опції <span class="function"><strong>debug_print_backtrace()</strong></span></strong></caption><tbody class="tbody"><tr><td>DEBUG_BACKTRACE_IGNORE_ARGS</td><td>Чи потрібно виключити ключ "args", тобто списки аргументів усіх функцій/методів, щоб зменшити витрату пам'яті.</td></tr></tbody></table>

`limit`

Аргумент використовується для обмеження кількості дзвінків функцій, які будуть виведені. За замовчуванням (`limit`\= ) буде виведено весь стек викликів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**debug\_print\_backtrace()\*\*\*\*

```php
<?php
// файл include.php

function a() {
    b();
}

function b() {
    c();
}

function c(){
    debug_print_backtrace();
}

a();

?>
```

```php
<?php
// файл test.php
// этот файл нужно запустить
include 'include.php';
?>
```

Висновок наведеного прикладу буде схожим на:

```
#0  c() called at [/tmp/include.php:10]
#1  b() called at [/tmp/include.php:6]
#2  a() called at [/tmp/include.php:17]
#3  include(/tmp/include.php) called at [/tmp/test.php:3]
```

### Дивіться також

-   [debug\_backtrace()](function.debug-backtrace.md) \- Генерує стек викликів функцій

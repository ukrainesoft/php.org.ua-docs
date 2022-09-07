---
navigation:
  - function.debug-backtrace.md: « debugbacktrace
  - function.error-clear-last.md: errorclearlast »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: debugprintbacktrace
---
# debugprintbacktrace

(PHP 5, PHP 7, PHP 8)

debugprintbacktrace — Виводить стек викликів функцій

### Опис

```methodsynopsis
debug_print_backtrace(int $options = 0, int $limit = 0): void
```

**debugprintbacktrace()** виводить стек викликів функцій. Виводить дзвінки функцій, імена включених/потрібних файлів та іншу інформацію з функцій ([eval()](function.eval.md)

### Список параметрів

`options`

Аргумент є бітовою маскою для наступних налаштувань:

<table class="doctable table"><caption><strong>Опції <span class="function"><strong>debug_print_backtrace()</strong></span></strong></caption><tbody class="tbody"><tr><td>DEBUG_BACKTRACE_IGNORE_ARGS</td><td>Чи потрібно виключити ключ "args", тобто списки аргументів усіх функцій/методів, щоб зменшити витрату пам'яті.</td></tr></tbody></table>

`limit`

Аргумент використовується для обмеження кількості дзвінків функцій, які будуть виведені. За замовчуванням (`limit``0`) буде виведено весь стек викликів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **debugprintbacktrace()****

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

Результатом виконання цього прикладу буде щось подібне:

```
#0  c() called at [/tmp/include.php:10]
#1  b() called at [/tmp/include.php:6]
#2  a() called at [/tmp/include.php:17]
#3  include(/tmp/include.php) called at [/tmp/test.php:3]
```

### Дивіться також

-   [debugbacktrace()](function.debug-backtrace.md) - Виводить стек викликів функцій у масив

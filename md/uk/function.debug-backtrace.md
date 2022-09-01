---
navigation:
  - ref.errorfunc.md: « Функции обработки ошибок
  - function.debug-print-backtrace.html: debugprintbacktrace »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: debugbacktrace
---
# debugbacktrace

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

debugbacktrace — Виводить стек викликів функцій у масив

### Опис

```methodsynopsis
debug_backtrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT, int $limit = 0): array
```

**debugbacktrace()** виводить стек викликів функцій PHP масив.

### Список параметрів

`options`

Аргумент є бітовою маскою для наступних налаштувань:

<table class="doctable table"><caption><strong>Опції <span class="function"><strong>debug_backtrace()</strong></span></strong></caption><tbody class="tbody"><tr><td>DEBUG_BACKTRACE_PROVIDE_OBJECT</td><td>Чи потрібно заповнювати дані для ключа object.</td></tr><tr><td>DEBUG_BACKTRACE_IGNORE_ARGS</td><td>Чи потрібно? виключити аргументи всіх функцій/методів у ключі "args" для зменшення витрати пам'яті.</td></tr></tbody></table>

`limit`

Аргумент використовується для обмеження кількості дзвінків функцій, які будуть виведені. За замовчуванням (`limit``0`) буде виведено весь стек викликів.

### Значення, що повертаються

Повертає масив вкладених асоціативних масивів (array). Опис елементів масиву наведено нижче:

**Список можливих елементів масивів, що повертаються функцією **debugbacktrace()****

| Имя | Тип | Описание |
| --- | --- | --- |
| function | string | Ім'я поточної функції. Дивіться також [FUNCTION](language.constants.predefined.md) |
| line | int | Поточний номер рядка. Дивіться також [LINE](language.constants.predefined.md) |
| file | string | Назва поточного файлу. Дивіться також [FILE](language.constants.predefined.md) |
| class | string | Ім'я поточного [класса](language.oop5.md). Дивіться також [CLASS](language.constants.predefined.md) |
| object | object | Поточний [об'єкт](language.oop5.md) |
| type | string | Поточний тип дзвінка функції. Якщо це виклик методу об'єкта, буде виведено "->". Якщо це виклик статичного методу класу, то "::". Якщо це простий виклик функції, нічого не виводиться. |
| args | array | При знаходженні всередині функції буде виведено список аргументів цієї функції. Якщо всередині файлу буде виведено список файлів, що включаються. |

### Приклади

**Приклад #1 Приклад використання **debugbacktrace()****

```php
<?php
// файл /tmp/a.php

function a_test($str)
{
    echo "\nПривет, $str";
    var_dump(debug_backtrace());
}

a_test('друг');
?>

<?php
// файл /tmp/b.php
include_once '/tmp/a.php';
?>
```

Результат аналогічний наведеному нижче, якщо запустити /tmp/b.php:

```
Привет, друг
array(2) {
[0]=>
array(4) {
    ["file"] => string(10) "/tmp/a.php"
    ["line"] => int(10)
    ["function"] => string(6) "a_test"
    ["args"]=>
    array(1) {
      [0] => &string(8) "друг"
    }
}
[1]=>
array(4) {
    ["file"] => string(10) "/tmp/b.php"
    ["line"] => int(2)
    ["args"] =>
    array(1) {
      [0] => string(10) "/tmp/a.php"
    }
    ["function"] => string(12) "include_once"
  }
}
```

### Дивіться також

-   [triggererror()](function.trigger-error.html) - Викликає помилку користувача/попередження/повідомлення
-   [debugprintbacktrace()](function.debug-print-backtrace.html) - Виводить стек викликів функцій

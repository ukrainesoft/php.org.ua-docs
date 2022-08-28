Виводить стек викликів функцій у масив

-   [« Функции обработки ошибок](ref.errorfunc.html)
    
-   [debug\_print\_backtrace »](function.debug-print-backtrace.html)
    
-   [PHP Manual](index.html)
    
-   [Функции обработки ошибок](ref.errorfunc.html)
    
-   Виводить стек викликів функцій у масив
    

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

| Имя      | Тип    | Описание                                                                                                                                                                                |
|----------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| function | string | Ім'я поточної функції. Дивіться також [\_\_FUNCTION\_\_](language.constants.predefined.html)                                                                                            |
| line     | int    | Поточний номер рядка. Дивіться також [\_\_LINE\_\_](language.constants.predefined.html)                                                                                                 |
| file     | string | Назва поточного файлу. Дивіться також [\_\_FILE\_\_](language.constants.predefined.html)                                                                                                |
| class    | string | Ім'я поточного [класса](language.oop5.html). Дивіться також [\_\_CLASS\_\_](language.constants.predefined.html)                                                                         |
| object   | object | Поточний [объект](language.oop5.html)                                                                                                                                                   |
| type     | string | Поточний тип дзвінка функції. Якщо це виклик методу об'єкта, буде виведено "->". Якщо це виклик статичного методу класу, то "::". Якщо це простий виклик функції, нічого не виводиться. |
| args     | array  | При знаходженні всередині функції буде виведено список аргументів цієї функції. Якщо всередині файлу буде виведено список файлів, що включаються.                                       |

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

-   [trigger\_error()](function.trigger-error.html) - Викликає помилку користувача/попередження/повідомлення
-   [debug\_print\_backtrace()](function.debug-print-backtrace.html) - Виводить стек викликів функцій
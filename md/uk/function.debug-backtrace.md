---
navigation:
  - ref.errorfunc.md: « Функції обробки помилок
  - function.debug-print-backtrace.md: debug\_print\_backtrace »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: debug\_backtrace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# debug\_backtrace

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

debug\_backtrace - Генерує стек викликів функцій

### Опис

```methodsynopsis
debug_backtrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT, int $limit = 0): array
```

Функция**debug\_backtrace()** генерує стек викликів функцій PHP.

### Список параметрів

`options`

Цей параметр – бітова маска для наступних налаштувань:

<table class="doctable table"><caption><strong>Опції <span class="function"><strong>debug_backtrace()</strong></span></strong></caption><tbody class="tbody"><tr><td>DEBUG_BACKTRACE_PROVIDE_OBJECT</td><td>Чи потрібно заповнювати ключ "object" (у виході масиві).</td></tr><tr><td>DEBUG_BACKTRACE_IGNORE_ARGS</td><td>Чи потрібно виключити ключ "args" (з вихідного масиву) з супутнім виключенням всіх аргументів функцій/методів, щоб зменшити витрату пам'яті.</td></tr></tbody></table>

> **Зауваження** :
> 
> Можливі чотири комбінації:
> 
> < /tr>
> 
> <table class="doctable table"><caption><strong>Опції <span class="function"><strong>debug_backtrace()</strong></span></strong></caption><tbody class="tbody"><tr><td><code class="code">debug_backtrace()</code></td><td rowspan="3" style="vertical-align: middle;">Заповнюються обидва ключі .</td></tr><tr><td><code class="code">debug_backtrace(DEBUG_BACKTRACE_PROVIDE_OBJECT)</code></td></tr><tr><td><code class=" code">debug_backtrace(1)</code></td></tr><tr><td><code class="code">debug_backtrace(0)</code></td><td style=" vertical-align: middle;">Не вмикається ключ <code class="literal">"object"</code> і заповнюється ключ <code class="literal">"args"</code>.</td></tr><tr><td><code class="code">debug_backtrace(DEBUG_BACKTRACE_IGNORE_ARGS)</code></td><td rowspan="2" style="vertical-align: middle;">Опускається ключ &lt; code class="literal"&gt;"object" <em>і</em> ключ <code class="literal">"args"</code>.</td></tr><tr><td><code class="code">debug_backtrace(2)</code></td></tr><tr><td><code class="code">debug_backtrace(DEBUG_BACKTRACE_PROVIDE_OBJECT|DEBUG_BACKTRACE_IGNORE_ARGS)</code></td><td rowspan="2" style="vertical-align: middle;">Заповнюється ключ <code class="literal">"object"</code> <em>і</em> опускається ключ <code class="literal">"args"</code>.</td></tr><tr><td><code class="code">debug_backtrace(3)</code></td></tr></tbody></table>

`limit`

Цим параметром можна обмежити кількість функцій, що повертаються. За замовчуванням параметр (`limit`\= ) — буде виведено весь стек викликів.

### Значення, що повертаються

Функція повертає масив вкладених асоціативних масивів (array). Опис елементів масиву наведено нижче:

**Список можливих елементів масивів, що повертаються функцією **debug\_backtrace()****

| Имя | Тип | Опис |
| --- | --- | --- |
| function | string | Ім'я поточної функції. Дивіться також [\_\_FUNCTION\_\_](language.constants.predefined.md) |
| line | int | Поточний номер рядка. Дивіться також [\_\_LINE\_\_](language.constants.predefined.md) |
| file | string | Назва поточного файлу. Дивіться також [\_\_FILE\_\_](language.constants.predefined.md) |
| class | string | Ім'я поточного [класу](language.oop5.md)Смотрите также[\_\_CLASS\_\_](language.constants.predefined.md) |
| object | object | Текущий[об'єкт](language.oop5.md) |
| type | string | Поточний тип дзвінка функції. Якщо це виклик методу об'єкта, буде повернуто значення "->". Якщо це виклик статичного методу класу, то "::". Якщо це простий дзвінок функції, нічого не повертається. |
| args | array | Якщо (функція **debug\_backtrace()**) викликана всередині функції, у цих ключах буде перераховано аргументи функцій. Якщо дзвінок здійснено всередині файлу, буде перераховано імена включених файлів. |

### Приклади

**Пример #1 Пример использования**debug\_backtrace()\*\*\*\*

```php
<?php
// файл /tmp/a.php

function a_test($str)
{
    echo "\nПривет, $str";
    var_dump(debug_backtrace());
}

a_test('друг');
?>

<?php
// файл /tmp/b.php
include_once '/tmp/a.php';
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

-   [trigger\_error()](function.trigger-error.md) \- Викликає помилку користувача/попередження/повідомлення
-   [debug\_print\_backtrace()](function.debug-print-backtrace.md) \- Виводить стек викликів функцій

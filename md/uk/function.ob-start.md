Увімкнення буферизації виводу

-   [« ob\_list\_handlers](function.ob-list-handlers.html)
    
-   [output\_add\_rewrite\_var »](function.output-add-rewrite-var.html)
    
-   [PHP Manual](index.html)
    
-   [Функции контроля вывода](ref.outcontrol.html)
    
-   Увімкнення буферизації виводу
    

# проstart

(PHP 4, PHP 5, PHP 7, PHP 8)

проstart — Увімкнення буферизації виводу

### Опис

```methodsynopsis
ob_start(callable $callback = null, int $chunk_size = 0, int $flags = PHP_OUTPUT_HANDLER_STDFLAGS): bool
```

Ця функція включає буферизацію виводу. Якщо буферизація виводу активна, жодного виводу скрипта не надсилається (крім заголовків), а зберігається у внутрішньому буфері.

Вміст цього внутрішнього буфера може бути скопійований у рядкову змінну, використовуючи [ob\_get\_contents()](function.ob-get-contents.html). Для виведення вмісту внутрішнього буфера слід використовувати [ob\_end\_flush()](function.ob-end-flush.html). Як альтернативу можна використовувати [ob\_end\_clean()](function.ob-end-clean.html) для чищення вмісту буфера.

**Увага**

Деякі веб-сервери (наприклад, Apache) змінюють робочу директорію скрипта під час виклику callback-функції. Ви можете повернути її назад, використовуючи `chdir(dirname($_SERVER['SCRIPT_FILENAME']))` в callback-функції.

Буфери виведення поміщаються у стек, тобто допускається виклик **проstart()** після виклику іншою активною **проstart()**. При цьому необхідно викликати [ob\_end\_flush()](function.ob-end-flush.html) відповідну кількість разів. Якщо активні кілька callback-функцій, висновок послідовно фільтрується кожної їх у порядку вкладення.

Якщо буферизація виводу ще активна, коли скрипт завершує роботу, PHP автоматично виводить вміст.

### Список параметрів

`callback`

Можна вказати необов'язковий параметр `callback`. Ця функція приймає рядок як аргумент і має також повернути рядок. Вона викликається при скиданні (надсиланні) або очищенні (за допомогою [ob\_flush()](function.ob-flush.html) [ob\_clean()](function.ob-clean.html) або подібних функцій) або якщо буфер виводу скидається до браузера після закінчення запиту. При виклику функції `callback`, вона отримує вміст буфера і, як очікується, повинна повернути оновлений вміст для виводу буфера, який буде відправлено браузеру. Якщо `callback` не є допустимою функцією, то ця функція поверне **`false`**. Опис функції для цього параметра:

```methodsynopsis
handler(string $buffer, int $phase = ?): string
```

`buffer`

Вміст буфера виводу.

`phase`

Бітова маска констант [**`PHP_OUTPUT_HANDLER_*`**](outcontrol.constants.html)

Якщо `callback` поверне **`false`**, то оригінальна інформація відправиться до браузера без змін.

Параметр `callback` може бути ігнорований передачею значення **`null`**

[ob\_end\_clean()](function.ob-end-clean.html) [ob\_end\_flush()](function.ob-end-flush.html) [ob\_clean()](function.ob-clean.html) [ob\_flush()](function.ob-flush.html) і **проstart()** не можуть викликатися з callback-функцій, тому що їхня поведінка непередбачувана. Якщо ви хочете видалити вміст буфера, поверніть "" (порожній рядок) з callback-функції. Ви також не можете використовувати функції буферизації виводу, такі як `print_r($expression, true)` або `highlight_file($filename, true)` з callback-функції.

> **Зауваження**
> 
> Функція [ob\_gzhandler()](function.ob-gzhandler.html) була введена для полегшення надсилання gz-кодованих даних браузерам, які підтримують стислі веб-сторінки . [ob\_gzhandler()](function.ob-gzhandler.html) визначає тип кодування вмісту, який приймає браузер, і повертає виведення відповідним чином.

`chunk_size`

Якщо передано необов'язковий параметр `chunk_size`, то буфер буде скинутий після будь-якого висновку, що перевищує або дорівнює за розміром `chunk_size`. Значення за замовчуванням `0` означає, що функція виведення буде викликана, коли буфер буде закрито.

`flags`

Параметр `flags` є бітовою маскою, яка керує операціями, які можна здійснювати над буфером виведення. За замовчуванням вона дозволяє буферу виводу бути очищеним, скинутим та віддаленим, що рівнозначне значенню **`PHP_OUTPUT_HANDLER_CLEANABLE`** **`PHP_OUTPUT_HANDLER_FLUSHABLE`** **`PHP_OUTPUT_HANDLER_REMOVABLE`** або **`PHP_OUTPUT_HANDLER_STDFLAGS`** як скорочення цієї комбінації.

Кожен прапор керує доступом до набору функцій, як описано нижче:

| Константа | Функции |
| --- | --- |
| **`PHP_OUTPUT_HANDLER_CLEANABLE`** | [ob\_clean()](function.ob-clean.html) [ob\_end\_clean()](function.ob-end-clean.html) і [ob\_get\_clean()](function.ob-get-clean.html) |
| **`PHP_OUTPUT_HANDLER_FLUSHABLE`** | [ob\_end\_flush()](function.ob-end-flush.html) [ob\_flush()](function.ob-flush.html) і [ob\_get\_flush()](function.ob-get-flush.html) |
| **`PHP_OUTPUT_HANDLER_REMOVABLE`** | [ob\_end\_clean()](function.ob-end-clean.html) [ob\_end\_flush()](function.ob-end-flush.html) і [ob\_get\_flush()](function.ob-get-flush.html) |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад callback-функції, визначеної користувачем**

```php
<?php

function callback($buffer)
{
  // заменить все яблоки апельсинами
  return (str_replace("яблоки", "апельсины", $buffer));
}

ob_start("callback");

?>
<html>
<body>
<p>Это всё равно что сравнить яблоки и апельсины.</p>
</body>
</html>
<?php

ob_end_flush();

?>
```

Результат виконання цього прикладу:

```
<html>
<body>
<p>Это всё равно что сравнить апельсины и апельсины.</p>
</body>
</html>
```

**Приклад #2 Створення буфера виводу, що не стирається.**

```php
<?php

ob_start(null, 0, PHP_OUTPUT_HANDLER_STDFLAGS ^ PHP_OUTPUT_HANDLER_REMOVABLE);

?>
```

### Дивіться також

-   [ob\_get\_contents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [ob\_end\_clean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
-   [ob\_end\_flush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [ob\_implicit\_flush()](function.ob-implicit-flush.html) - Увімкнення/вимкнення неявного скидання
-   [ob\_gzhandler()](function.ob-gzhandler.html) - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
-   [ob\_iconv\_handler()](function.ob-iconv-handler.html) - Перетворює символи з поточного кодування на кодування вихідного буфера
-   [mb\_output\_handler()](function.mb-output-handler.html) - Callback-функція, що перетворює кодування символів у вихідному буфері
-   [ob\_tidyhandler()](function.ob-tidyhandler.html) - Функція зворотного виклику obstart для відновлення буфера
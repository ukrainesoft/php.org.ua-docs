---
navigation:
  - function.ob-list-handlers.html: « oblisthandlers
  - function.output-add-rewrite-var.html: outputaddrewritevar »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: проstart
---
# проstart

(PHP 4, PHP 5, PHP 7, PHP 8)

проstart — Увімкнення буферизації виводу

### Опис

```methodsynopsis
ob_start(callable $callback = null, int $chunk_size = 0, int $flags = PHP_OUTPUT_HANDLER_STDFLAGS): bool
```

Ця функція включає буферизацію виводу. Якщо буферизація виводу активна, жодного виводу скрипта не надсилається (крім заголовків), а зберігається у внутрішньому буфері.

Вміст цього внутрішнього буфера може бути скопійований у рядкову змінну, використовуючи [проgetcontents()](function.ob-get-contents.html). Для виведення вмісту внутрішнього буфера слід використовувати [проendflush()](function.ob-end-flush.html). Як альтернативу можна використовувати [проendclean()](function.ob-end-clean.html) для чищення вмісту буфера.

**Увага**

Деякі веб-сервери (наприклад, Apache) змінюють робочу директорію скрипта під час виклику callback-функції. Ви можете повернути її назад, використовуючи `chdir(dirname($_SERVER['SCRIPT_FILENAME']))` в callback-функції.

Буфери виведення поміщаються у стек, тобто допускається виклик **проstart()** після виклику іншою активною **проstart()**. При цьому необхідно викликати [проendflush()](function.ob-end-flush.html) відповідну кількість разів. Якщо активні кілька callback-функцій, висновок послідовно фільтрується кожної їх у порядку вкладення.

Якщо буферизація виводу ще активна, коли скрипт завершує роботу, PHP автоматично виводить вміст.

### Список параметрів

`callback`

Можна вказати необов'язковий параметр `callback`. Ця функція приймає рядок як аргумент і має також повернути рядок. Вона викликається при скиданні (надсиланні) або очищенні (за допомогою [проflush()](function.ob-flush.html) [проclean()](function.ob-clean.html) або подібних функцій) або якщо буфер виводу скидається до браузера після закінчення запиту. При виклику функції `callback`, вона отримує вміст буфера і, як очікується, повинна повернути оновлений вміст для виводу буфера, який буде відправлено браузеру. Якщо `callback` не є допустимою функцією, то ця функція поверне **`false`**. Опис функції для цього параметра:

```methodsynopsis
handler(string $buffer, int $phase = ?): string
```

`buffer`

Вміст буфера виводу.

`phase`

Бітова маска констант [**`PHP_OUTPUT_HANDLER_*`**](outcontrol.constants.md)

Якщо `callback` поверне **`false`**, то оригінальна інформація відправиться до браузера без змін.

Параметр `callback` може бути ігнорований передачею значення **`null`**

[проendclean()](function.ob-end-clean.html) [проendflush()](function.ob-end-flush.html) [проclean()](function.ob-clean.html) [проflush()](function.ob-flush.html) і **проstart()** не можуть викликатися з callback-функцій, тому що їхня поведінка непередбачувана. Якщо ви хочете видалити вміст буфера, поверніть "" (порожній рядок) з callback-функції. Ви також не можете використовувати функції буферизації виводу, такі як `print_r($expression, true)` або `highlight_file($filename, true)` з callback-функції.

> **Зауваження**
> 
> Функція [проgzhandler()](function.ob-gzhandler.html) була введена для полегшення надсилання gz-кодованих даних браузерам, які підтримують стислі веб-сторінки . [проgzhandler()](function.ob-gzhandler.html) визначає тип кодування вмісту, який приймає браузер, і повертає виведення відповідним чином.

`chunk_size`

Якщо передано необов'язковий параметр `chunk_size`, то буфер буде скинутий після будь-якого висновку, що перевищує або дорівнює за розміром `chunk_size`. Значення за замовчуванням `0` означає, що функція виведення буде викликана, коли буфер буде закрито.

`flags`

Параметр `flags` є бітовою маскою, яка керує операціями, які можна здійснювати над буфером виведення. За замовчуванням вона дозволяє буферу виводу бути очищеним, скинутим та віддаленим, що рівнозначне значенню **`PHP_OUTPUT_HANDLER_CLEANABLE`** **`PHP_OUTPUT_HANDLER_FLUSHABLE`** **`PHP_OUTPUT_HANDLER_REMOVABLE`** або **`PHP_OUTPUT_HANDLER_STDFLAGS`** як скорочення цієї комбінації.

Кожен прапор керує доступом до набору функцій, як описано нижче:

| Константа | Функции |
| --- | --- |
| **`PHP_OUTPUT_HANDLER_CLEANABLE`** | [проclean()](function.ob-clean.html) [проendclean()](function.ob-end-clean.html) і [проgetclean()](function.ob-get-clean.html) |
| **`PHP_OUTPUT_HANDLER_FLUSHABLE`** | [проendflush()](function.ob-end-flush.html) [проflush()](function.ob-flush.html) і [проgetflush()](function.ob-get-flush.html) |
| **`PHP_OUTPUT_HANDLER_REMOVABLE`** | [проendclean()](function.ob-end-clean.html) [проendflush()](function.ob-end-flush.html) і [проgetflush()](function.ob-get-flush.html) |

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

-   [проgetcontents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
-   [проendclean()](function.ob-end-clean.html) - Очистити (стерти) буфер виведення та вимкнути буферизацію виводу
-   [проendflush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу
-   [про implicit flush()](function.ob-implicit-flush.html) - Увімкнення/вимкнення неявного скидання
-   [проgzhandler()](function.ob-gzhandler.html) - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
-   [проiconvhandler()](function.ob-iconv-handler.html) - Перетворює символи з поточного кодування на кодування вихідного буфера
-   [мбoutputhandler()](function.mb-output-handler.html) - Callback-функція, що перетворює кодування символів у вихідному буфері
-   [проtidyhandler()](function.ob-tidyhandler.html) - Функція зворотного виклику obstart для відновлення буфера

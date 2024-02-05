---
navigation:
  - function.sapi-windows-set-ctrl-handler.md: « sapi\_windows\_set\_ctrl\_handler
  - function.show-source.md: show\_source »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_vt100\_support
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_vt100\_support

(PHP 7 >= 7.2.0, PHP 8)

sapi\_windows\_vt100\_support — Отримати або встановити підтримку VT100 для заданого потоку, пов'язаного з буфером виведення консолі Windows

### Опис

```methodsynopsis
sapi_windows_vt100_support(resource $stream, ?bool $enable = null): bool
```

Якщо параметр `enable`равен\*\*`null`\*\*, функція повертає **`true`**или**`false`** в залежності від того, дозволені чи ні керуючі послідовності VT100 для `stream`

Якщо параметр `enable` є логічним значенням (bool), функція спробує увімкнути або вимкнути функціональність VT100 для потоку `stream`. У цьому випадку функція поверне **`true`**или**`false`** залежно від успішності виконання.

При старті PHP намагається включити VT100 для потоків **`STDOUT`**и**`STDERR`**. Але якщо, наприклад, ці потоки перенаправлені у файл, то підтримка VT100 може включитися.

Якщо включена підтримка VT100, можна використовувати керуючі послідовності, оскільки вони відомі терміналу. Вони дозволяють змінювати виведення терміналу. У Windows ці послідовності відомі як "Console Virtual Terminal Sequences".

**Увага**

Ця функція використовує реалізацію прапора **`ENABLE_VIRTUAL_TERMINAL_PROCESSING`** у Windows 10 API, отже функціональність VT100 може бути недоступна у старіших версіях Windows.

### Список параметрів

`stream`

Потік, з яким працюватиме функція.

`enable`

Якщо є логічним значенням (bool), то має бути або **`true`**, либо\*\*`false`\*\*, для включення та відключення VT100 відповідно.

### Значення, що повертаються

Якщо параметр `enable`равен\*\*`null`\*\*, функція повертає **`true`**или**`false`** залежно від того, дозволені чи ні керуючі послідовності VT100

Якщо параметр `enable` є логічним значенням (bool): Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `enable` тепер допускає значення null. |

### Приклади

\*\*Приклад #1 Стан \*\*sapi\_windows\_vt100\_support()**по умолчанию**

По умолчанию, для\*\*`STDOUT`**и**`STDERR`\*\*поддержка VT100 включена.

php -r "var\_export(sapi\_windows\_vt100\_support(STDOUT));echo ' ';var\_export(sapi\_windows\_vt100\_support(STDERR));"

Висновок наведеного прикладу буде схожим на:

```
true true
```

Якщо потік перенаправлений, то підтримка VT100 буде вимкнена:

php -r "var\_export(sapi\_windows\_vt100\_support(STDOUT));echo ' ';var\_export(sapi\_windows\_vt100\_support(STDERR));" 2>NUL

Висновок наведеного прикладу буде схожим на:

true false

**Пример #2 Изменение состояния с помощью**sapi\_windows\_vt100\_support()\*\*\*\*

Ви не можете включити підтримку VT100 для **`STDOUT`**или**`STDERR`** якщо ці потоки перенаправлені.

php -r "var\_export(sapi\_windows\_vt100\_support(STDOUT, true));echo ' ';var\_export(sapi\_windows\_vt100\_support(STDERR, true));" 2>NUL

Висновок наведеного прикладу буде схожим на:

```
true false
```

**Приклад #3 Приклад використання за допомогою VT100**

```php
<?php
$out = fopen('php://stdout','w');
fwrite($out, 'Just forgot a lettr.');
// Переместить курсор на две позиции назад
fwrite($out, "\033[2D");
// Вставляет один пробел, сдвигая существующий текст вправо -> Просто забыли букву.
fwrite($out, "\033[1@");
fwrite($out, 'e');
?>
```

Результат виконання наведеного прикладу:

```
Just forgot a letter.
```

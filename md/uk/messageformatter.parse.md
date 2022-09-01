---
navigation:
  - messageformatter.parsemessage.html: '« MessageFormatter::parseMessage'
  - messageformatter.setpattern.html: 'MessageFormatter::setPattern »'
  - index.html: PHP Manual
  - class.messageformatter.html: MessageFormatter
title: 'MessageFormatter::parse'
---
# MessageFormatter::parse

# msgfmtparse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::parse -- msgfmtparse — Розбирає рядок згідно шаблону

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::parse(string $string): array|false
```

Процедурний стиль

```methodsynopsis
msgfmt_parse(MessageFormatter $formatter, string $string): array|false
```

Розбирає вхідний рядок (string) і повертає всі вилучені елементи як масиву (array).

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.html)

`string`

Рядок (string) для розбору.

### Значення, що повертаються

Масив (array), що містить вилучені елементи або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmtparse()****

```php
<?php
$fmt = msgfmt_create('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = msgfmt_parse($fmt, "4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = msgfmt_create('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = msgfmt_parse($fmt, "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = $fmt->parse("4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = new MessageFormatter('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = $fmt->parse("4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

Результат виконання цього прикладу:

```
array (
  0 => 4560,
  1 => 123,
  2 => 37.073,
)
array (
  0 => 4560,
  1 => 123,
  2 => 37.073,
)
```

### Дивіться також

-   [msgfmtcreate()](messageformatter.create.html) - Створює засіб форматування повідомлень
-   [msgfmtformat()](messageformatter.format.html) - Форматує повідомлення
-   [msgfmtparsemessage()](messageformatter.parsemessage.html) - швидко розбирає вхідний рядок

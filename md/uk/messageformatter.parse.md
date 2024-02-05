---
navigation:
  - messageformatter.parsemessage.md: '« MessageFormatter::parseMessage'
  - messageformatter.setpattern.md: 'MessageFormatter::setPattern »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::parse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::parse

# msgfmt\_parse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::parse -- msgfmt\_parse — Розбирає рядок згідно шаблону

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

Об'єкт [MessageFormatter](class.messageformatter.md)

`string`

Рядок (string) для розбору.

### Значення, що повертаються

Масив (array), що містить вилучені елементи або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** msgfmt\_parse()\*\*\*\*

```php
<?php
$fmt = msgfmt_create('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = msgfmt_parse($fmt, "4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = msgfmt_create('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = msgfmt_parse($fmt, "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
$res = $fmt->parse("4,560 monkeys on 123 trees make 37.073 monkeys per tree");
var_export($res);

$fmt = new MessageFormatter('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
$res = $fmt->parse("4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");
var_export($res);
?>
```

Результат виконання наведеного прикладу:

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

-   [msgfmt\_create()](messageformatter.create.md) \- Створює засіб форматування повідомлень
-   [msgfmt\_format()](messageformatter.format.md) \- Форматує повідомлення
-   [msgfmt\_parse\_message()](messageformatter.parsemessage.md) \- швидко розбирає вхідний рядок

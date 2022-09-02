---
navigation:
  - messageformatter.parse.md: '« MessageFormatter::parse'
  - class.intlcalendar.md: IntlCalendar »
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::setPattern'
---
# MessageFormatter::setPattern

# msgfmtsetpattern

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::setPattern -- msgfmtsetpattern — Встановлює шаблон, який використовує засіб форматування.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::setPattern(string $pattern): bool
```

Процедурний стиль

```methodsynopsis
msgfmt_set_pattern(MessageFormatter $formatter, string $pattern): bool
```

Встановлює шаблон, який використовується засобом форматування.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.md)

`pattern`

Рядок (string) шаблону для використання у цьому засобі форматування повідомлення. У шаблоні використовується "дружній до апострофів" синтаксис; докладніше дивіться у розділі [» Quoting/Escaping](https://unicode-org.github.io/icu/userguide/format_parse/messages/#quotingescaping)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmtsetpattern()****

```php
<?php
$fmt = msgfmt_create( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatting result: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";

msgfmt_set_pattern( $fmt, "{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . msgfmt_get_pattern( $fmt ) . "'\n";
echo "Formatted number: " . msgfmt_format( $fmt, array(123, 456) ) . "\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter( "en_US", "{0, number} monkeys on {1, number} trees" );
echo "Default pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatting result: " . $fmt->format(array(123, 456)) . "\n";

$fmt->setPattern("{0, number} trees hosting {1, number} monkeys" );
echo "New pattern: '" . $fmt->getPattern() . "'\n";
echo "Formatted number: " . $fmt->format(array(123, 456)) . "\n";
?>
```

Результат виконання цього прикладу:

```
Default pattern: '{0,number} monkeys on {1,number} trees'
Formatting result: 123 monkeys on 456 trees
New pattern: '{0,number} trees hosting {1,number} monkeys'
Formatted number: 123 trees hosting 456 monkeys
```

### Дивіться також

-   [msgfmtcreate()](messageformatter.create.md) - Створює засіб форматування повідомлень
-   [msgfmtgetpattern()](messageformatter.getpattern.md) - Повертає шаблон, який використовується засобом форматування

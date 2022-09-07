---
navigation:
  - class.messageformatter.md: « MessageFormatter
  - messageformatter.formatmessage.md: 'MessageFormatter::formatMessage »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::create'
---
# MessageFormatter::create

# MessageFormatter::construct

# msgfmtcreate

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::create -- MessageFormatter::construct - msgfmtcreate — Створює засіб форматування повідомлень

### Опис

Об'єктно-орієнтований стиль (метод)

```methodsynopsis
public static MessageFormatter::create(string $locale, string $pattern): ?MessageFormatter
```

Об'єктно-орієнтований стиль (конструктор):

public **MessageFormatter::construct**(string `$locale`, string `$pattern`

Процедурний стиль

```methodsynopsis
msgfmt_create(string $locale, string $pattern): ?MessageFormatter
```

Створює засіб форматування повідомлень.

### Список параметрів

`locale`

Локаль, яка використовується при форматуванні аргументів

`pattern`

Рядок (string) шаблон для вставлення аргументів. У шаблоні використовується "дружній до апострофів" синтаксис; докладніше дивіться у розділі [» Quoting/Escaping](https://unicode-org.github.io/icu/userguide/format_parse/messages/#quotingescaping)

### Значення, що повертаються

Об'єкт [MessageFormatter](class.messageformatter.md) або **`null`** у разі виникнення помилки.

### Помилки

При виклику як конструктор у разі виникнення помилки викидається виняток [IntlException](class.intlexception.md)

### Приклади

**Приклад #1 Приклад використання **msgfmtcreate()****

```php
<?php
$fmt = msgfmt_create("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
$fmt = msgfmt_create("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo $fmt->format(array(4560, 123, 4560/123));
$fmt = new MessageFormatter("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo $fmt->format(array(4560, 123, 4560/123));
?>
```

Результат виконання цього прикладу:

```
4,560 monkeys on 123 trees make 37.073 monkeys per tree
4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum
```

### Дивіться також

-   [msgfmtformat()](messageformatter.format.md) - Форматує повідомлення
-   [msgfmtparse()](messageformatter.parse.md) - Розбирає рядок згідно шаблону
-   [msgfmtgeterrorcode()](messageformatter.geterrorcode.md) - Повертає код помилки останньої операції
-   [msgfmtgeterrormessage()](messageformatter.geterrormessage.md) - Повертає текст помилки останньої операції

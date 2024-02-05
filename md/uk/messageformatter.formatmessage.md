---
navigation:
  - messageformatter.create.md: '« MessageFormatter::create'
  - messageformatter.format.md: 'MessageFormatter::format »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::formatMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::formatMessage

# msgfmt\_format\_message

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::formatMessage -- msgfmt\_format\_message — Швидко форматує повідомлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static MessageFormatter::formatMessage(string $locale, string $pattern, array $values): string|false
```

Процедурний стиль

```methodsynopsis
msgfmt_format_message(string $locale, string $pattern, array $values): string|false
```

Функція швидкого форматування, яка форматує рядок без необхідності створювати об'єкт форматування. Використовуйте цю функцію, коли форматування виконується лише один раз і не потребує збереження параметрів або стану, а також коли необхідно налаштувати висновок, надавши додатковий контекст безпосередньо для ICU.

### Список параметрів

`locale`

Локаль, що використовується для форматування частин, що залежать від локалі

`pattern`

Рядок (string) шаблону для вставлення аргументів. У шаблоні використовується "дружній до апострофів" синтаксис; докладніше дивіться у розділі [» Quoting/Escaping](https://unicode-org.github.io/icu/userguide/format_parse/messages/#quotingescaping)

`values`

Масив значень (array) для вставлення у рядок формату (string).

### Значення, що повертаються

Рядок відформатованого шаблону або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** msgfmt\_format\_message()\*\*\*\*

```php
<?php
echo msgfmt_format_message("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo msgfmt_format_message("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
echo msgfmt_format_message("en", 'You finished {place, selectordinal, one {#st} two {#nd} few {#rd} other {#th}}!', ['place' => 3]), "\n";
echo msgfmt_format_message("en",
        "There {apple, plural,
            =0 {are no apples}
            =1 {is one apple...}
            other {are # apples!}
        }",
    ['apple' => 0]
), "\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo MessageFormatter::formatMessage("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo MessageFormatter::formatMessage("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
echo MessageFormatter::formatMessage("en", 'You finished {place, selectordinal, one {#st} two {#nd} few {#rd} other {#th}}!', ['place' => 3]), "\n";
echo MessageFormatter::formatMessage("en",
        "There {apple, plural,
            =0 {are no apples}
            =1 {is one apple...}
            other {are # apples!}
        }",
    ['apple' => 0]
), "\n";
?>
```

Результат виконання наведеного прикладу:

```
4,560 monkeys on 123 trees make 37.073 monkeys per tree
4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum
You finished 3rd!
There are no apples
```

**Приклад #3 Приклад використання ICU для форматування валюти із загальним та з вузьким символом валюти**

Requires ICU ≥ 67.

```php
<?php
echo msgfmt_format_message("cs_CZ", "{0, number, :: currency/CAD}", array(123.45));
echo msgfmt_format_message("cs_CZ", "{0, number, :: currency/CAD unit-width-narrow}", array(123.45));
```

Результат виконання наведеного прикладу:

```
123,45 CA$
123,45 $
```

### Дивіться також

-   [msgfmt\_create()](messageformatter.create.md) \- Створює засіб форматування повідомлень
-   [msgfmt\_parse()](messageformatter.parse.md) \- Розбирає рядок згідно шаблону
-   [msgfmt\_get\_error\_code()](messageformatter.geterrorcode.md) \- Повертає код помилки останньої операції
-   [msgfmt\_get\_error\_message()](messageformatter.geterrormessage.md) \- Повертає текст помилки останньої операції

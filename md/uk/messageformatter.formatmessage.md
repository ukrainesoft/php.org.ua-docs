Швидко форматує повідомлення

-   [« MessageFormatter::create](messageformatter.create.html)
    
-   [MessageFormatter::format »](messageformatter.format.html)
    
-   [PHP Manual](index.html)
    
-   [MessageFormatter](class.messageformatter.html)
    
-   Швидко форматує повідомлення
    

# MessageFormatter::formatMessage

# msgfmtformatmessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::formatMessage -- msgfmtformatmessage — Швидко форматує повідомлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static MessageFormatter::formatMessage(string $locale, string $pattern, array $values): string|false
```

Процедурний стиль

```methodsynopsis
msgfmt_format_message(string $locale, string $pattern, array $values): string|false
```

Функція швидкого форматування, яка форматує рядок без необхідності створювати об'єкт форматування. Використовуйте цю функцію, коли форматування виконується лише один раз і не потребує збереження параметрів або стану.

### Список параметрів

`locale`

Локаль, що використовується для форматування частин, що залежать від локалі

`pattern`

Рядок (string) шаблону для вставлення аргументів. У шаблоні використовується "дружній до апострофів" синтаксис; докладніше дивіться у розділі [» Quoting/Escaping](https://unicode-org.github.io/icu/userguide/format_parse/messages/#quotingescaping)

`values`

Масив значень (array) для вставлення у рядок формату (string).

### Значення, що повертаються

Рядок відформатованого шаблону або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmtformatmessage()****

```php
<?php
echo msgfmt_format_message("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo msgfmt_format_message("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
echo MessageFormatter::formatMessage("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree\n", array(4560, 123, 4560/123));
echo MessageFormatter::formatMessage("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum\n", array(4560, 123, 4560/123));
?>
```

Результат виконання цього прикладу:

```
4,560 monkeys on 123 trees make 37.073 monkeys per tree
4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum
```

### Дивіться також

-   [msgfmtcreate()](messageformatter.create.html) - Створює засіб форматування повідомлень
-   [msgfmtparse()](messageformatter.parse.html) - Розбирає рядок згідно шаблону
-   [msgfmtgeterrorcode()](messageformatter.geterrorcode.html) - Повертає код помилки останньої операції
-   [msgfmtgeterrormessage()](messageformatter.geterrormessage.html) - Повертає текст помилки останньої операції
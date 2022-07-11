- [« MessageFormatter::getPattern](messageformatter.getpattern.md)
- [MessageFormatter::parse »](messageformatter.parse.md)

- [PHP Manual](index.md)
- [MessageFormatter](class.messageformatter.md)
- швидко розбирає вхідний рядок

# MessageFormatter::parseMessage

#msgfmt_parse_message

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL intl = 1.0.0)

MessageFormatter::parseMessage -- msgfmt_parse_message -- Швидко
розбирає вхідний рядок

### Опис

Об'єктно-орієнтований стиль

public static **MessageFormatter::parseMessage**(string `$locale`,
string `$pattern`, string `$message`): array\|false

Процедурний стиль

**msgfmt_parse_message**(string `$locale`, string `$pattern`, string
`$message`): array\|false

Розбирає вхідний рядок без створення об'єкта форматування.
Використовуйте цю функцію, коли операція форматування виконується
лише один раз і не потребує збереження параметрів або стану.

### Список параметрів

`locale`
Локаль, що використовується для аналізу частин, що залежать від локалі

`pattern`
Шаблон, що використовується для аналізу `message`.

`message`
Рядок (string) для розбору, що відповідає `pattern`.

### Значення, що повертаються

Масив (array), що містить вилучені елементи або **`false`** у разі
виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmt_parse_message()****

` <?php$fmt = msgfmt_parse_message('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree",                            "4,560 monkeys on 123 trees make 37.073 monkeys per tree");var_export($fmt);$fmt = msgfmt_parse_message('de', "{0,number,integer} Affen auf {1,number,integer} Bäumen sind    "4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum");var_export($fmt);?> `

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

` <?php$fmt = MessageFormatter::parseMessage('en_US', "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree",                            "4,560 monkeys on 123 trees make 37.073 monkeys per tree");var_export($fmt);$fmt = MessageFormatter::parseMessage('de', "{0,number,integer} Affen auf {1, } Affen pro Baum",                            "4.560 Affen auf 123 Bäu;

Результат виконання цього прикладу:

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

### Дивіться також

- [msgfmt_create()](messageformatter.create.md) - Створює засіб
форматування повідомлень
- [msgfmt_format_message()](messageformatter.formatmessage.md) -
Швидко форматує повідомлення
- [msgfmt_parse()](messageformatter.parse.md) - Розбирає рядок
згідно шаблону

Форматує повідомлення

-   [« MessageFormatter::formatMessage](messageformatter.formatmessage.html)
    
-   [MessageFormatter::getErrorCode »](messageformatter.geterrorcode.html)
    
-   [PHP Manual](index.html)
    
-   [MessageFormatter](class.messageformatter.html)
    
-   Форматує повідомлення
    

# MessageFormatter::format

# msgfmtformat

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::format -- msgfmtformat — Форматує повідомлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::format(array $values): string|false
```

Процедурний стиль

```methodsynopsis
msgfmt_format(MessageFormatter $formatter, array $values): string|false
```

Форматує повідомлення, підставляючи дані у рядок формату відповідно до правил локалі.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.html)

`values`

Аргументи для вставки у рядок формату

### Значення, що повертаються

Відформатований рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmtformat()****

```php
<?php
$fmt = msgfmt_create("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
$fmt = msgfmt_create("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo msgfmt_format($fmt, array(4560, 123, 4560/123));
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter("en_US", "{0,number,integer} monkeys on {1,number,integer} trees make {2,number} monkeys per tree");
echo $fmt->format(array(4560, 123, 4560/123));
$fmt = new MessageFormatter("de", "{0,number,integer} Affen auf {1,number,integer} Bäumen sind {2,number} Affen pro Baum");
echo $fmt->format(array(4560, 123, 4560/123));
?>
```

Результат виконання цього прикладу:

```
4,560 monkeys on 123 trees make 37.073 monkeys per tree
4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum
```

### Дивіться також

-   [msgfmt\_create()](messageformatter.create.html) - Створює засіб форматування повідомлень
-   [msgfmt\_parse()](messageformatter.parse.html) - Розбирає рядок згідно шаблону
-   [msgfmt\_format\_message()](messageformatter.formatmessage.html) - Швидко форматує повідомлення
-   [msgfmt\_get\_error\_code()](messageformatter.geterrorcode.html) - Повертає код помилки останньої операції
-   [msgfmt\_get\_error\_message()](messageformatter.geterrormessage.html) - Повертає текст помилки останньої операції
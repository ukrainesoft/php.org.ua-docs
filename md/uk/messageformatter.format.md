---
navigation:
  - messageformatter.formatmessage.md: '« MessageFormatter::formatMessage'
  - messageformatter.geterrorcode.md: 'MessageFormatter::getErrorCode »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::format'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::format

# msgfmt\_format

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::format -- msgfmt\_format — Форматує повідомлення

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

Об'єкт [MessageFormatter](class.messageformatter.md)

`values`

Аргументи для вставки у рядок формату

### Значення, що повертаються

Відформатований рядок або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** msgfmt\_format()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
4,560 monkeys on 123 trees make 37.073 monkeys per tree
4.560 Affen auf 123 Bäumen sind 37,073 Affen pro Baum
```

### Дивіться також

-   [msgfmt\_create()](messageformatter.create.md) \- Створює засіб форматування повідомлень
-   [msgfmt\_parse()](messageformatter.parse.md) \- Розбирає рядок згідно шаблону
-   [msgfmt\_format\_message()](messageformatter.formatmessage.md) \- Швидко форматує повідомлення
-   [msgfmt\_get\_error\_code()](messageformatter.geterrorcode.md) \- Повертає код помилки останньої операції
-   [msgfmt\_get\_error\_message()](messageformatter.geterrormessage.md) \- Повертає текст помилки останньої операції

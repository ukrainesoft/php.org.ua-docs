---
navigation:
  - messageformatter.geterrormessage.md: '« MessageFormatter::getErrorMessage'
  - messageformatter.getpattern.md: 'MessageFormatter::getPattern »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::getLocale'
---
# MessageFormatter::getLocale

# msgfmtgetlocale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getLocale -- msgfmtgetlocale — Повертає локаль, для якої було створено засіб форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::getLocale(): string
```

Процедурний стиль

```methodsynopsis
msgfmt_get_locale(MessageFormatter $formatter): string
```

Повертає локаль, на яку було створено засіб форматування.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.md)

### Значення, що повертаються

Ім'я локали.

### Приклади

**Приклад #1 Приклад використання **msgfmtgetlocale()****

```php
<?php
$fmt = msgfmt_create('en_US', "Number {0,number}");
echo msgfmt_get_locale($fmt);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter('en_US', "Number {0,number}");
echo $fmt->getLocale();
?>
```

Результат виконання цього прикладу:

```
en_US
```

### Дивіться також

-   [msgfmtcreate()](messageformatter.create.md) - Створює засіб форматування повідомлень

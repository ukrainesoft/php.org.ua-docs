---
navigation:
  - messageformatter.geterrormessage.md: '« MessageFormatter::getErrorMessage'
  - messageformatter.getpattern.md: 'MessageFormatter::getPattern »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::getLocale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::getLocale

# msgfmt\_get\_locale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getLocale -- msgfmt\_get\_locale — Повертає локаль, для якої було створено засіб форматування

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

**Пример #1 Пример использования**msgfmt\_get\_locale()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
en_US
```

### Дивіться також

-   [msgfmt\_create()](messageformatter.create.md) \- Створює засіб форматування повідомлень

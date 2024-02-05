---
navigation:
  - messageformatter.geterrorcode.md: '« MessageFormatter::getErrorCode'
  - messageformatter.getlocale.md: 'MessageFormatter::getLocale »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::getErrorMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::getErrorMessage

# msgfmt\_get\_error\_message

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getErrorMessage -- msgfmt\_get\_error\_message — Повертає помилку останньої операції.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::getErrorMessage(): string
```

Процедурний стиль

```methodsynopsis
msgfmt_get_error_message(MessageFormatter $formatter): string
```

Повертає помилку останньої операції.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.md)

### Значення, що повертаються

Опис останньої помилки.

### Приклади

**Пример #1 Пример использования**msgfmt\_get\_error\_message()\*\*\*\*

```php
<?php
$fmt = msgfmt_create("en_US", "{0, number} monkeys on {1, number} trees");
$str = msgfmt_format($fmt, array());
if(!$str) {
    echo "ERROR: ".msgfmt_get_error_message($fmt) . " (" . msgfmt_get_error_code($fmt) . ")\n";
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter("en_US", "{0, number} monkeys on {1, number} trees");
$str = $fmt->format(array());
if(!$str) {
    echo "ERROR: ".$fmt->getErrorMessage() . " (" . $fmt->getErrorCode() . ")\n";
}
?>
```

Результат виконання наведеного прикладу:

```
ERROR: msgfmt_format: not enough parameters: U_ILLEGAL_ARGUMENT_ERROR (1)
```

### Дивіться також

-   [msgfmt\_get\_error\_code()](messageformatter.geterrorcode.md) \- Повертає код помилки останньої операції
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою

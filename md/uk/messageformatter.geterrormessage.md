---
navigation:
  - messageformatter.geterrorcode.html: '« MessageFormatter::getErrorCode'
  - messageformatter.getlocale.html: 'MessageFormatter::getLocale »'
  - index.html: PHP Manual
  - class.messageformatter.html: MessageFormatter
title: 'MessageFormatter::getErrorMessage'
---
# MessageFormatter::getErrorMessage

# msgfmtgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getErrorMessage -- msgfmtgeterrormessage — Повертає текст помилки останньої операції

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

Об'єкт [MessageFormatter](class.messageformatter.html)

### Значення, що повертаються

Опис останньої помилки.

### Приклади

**Приклад #1 Приклад використання **msgfmtgeterrormessage()****

```php
<?php
$fmt = msgfmt_create("en_US", "{0, number} monkeys on {1, number} trees");
$str = msgfmt_format($fmt, array());
if(!$str) {
    echo "ERROR: ".msgfmt_get_error_message($fmt) . " (" . msgfmt_get_error_code($fmt) . ")\n";
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new MessageFormatter("en_US", "{0, number} monkeys on {1, number} trees");
$str = $fmt->format(array());
if(!$str) {
    echo "ERROR: ".$fmt->getErrorMessage() . " (" . $fmt->getErrorCode() . ")\n";
}
?>
```

Результат виконання цього прикладу:

```
ERROR: msgfmt_format: not enough parameters: U_ILLEGAL_ARGUMENT_ERROR (1)
```

### Дивіться також

-   [msgfmtgeterrorcode()](messageformatter.geterrorcode.html) - Повертає код помилки останньої операції
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою

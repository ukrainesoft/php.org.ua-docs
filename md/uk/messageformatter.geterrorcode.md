---
navigation:
  - messageformatter.format.html: '« MessageFormatter::format'
  - messageformatter.geterrormessage.html: 'MessageFormatter::getErrorMessage »'
  - index.html: PHP Manual
  - class.messageformatter.html: MessageFormatter
title: 'MessageFormatter::getErrorCode'
---
# MessageFormatter::getErrorCode

# msgfmtgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getErrorCode -- msgfmtgeterrorcode — Повертає код помилки останньої операції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
msgfmt_get_error_code(MessageFormatter $formatter): int
```

Повертає код помилки останньої операції.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.md)

### Значення, що повертаються

Код помилки є одним із значень UErrorCode. Початкове значення - UZEROERROR.

### Дивіться також

-   [msgfmtgeterrormessage()](messageformatter.geterrormessage.md) - Повертає текст помилки останньої операції
-   [intlgeterrorcode()](function.intl-get-error-code.md) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.md) - Перевірити, чи є код помилки ознакою збою

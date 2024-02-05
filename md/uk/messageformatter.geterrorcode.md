---
navigation:
  - messageformatter.format.md: '« MessageFormatter::format'
  - messageformatter.geterrormessage.md: 'MessageFormatter::getErrorMessage »'
  - index.md: PHP Manual
  - class.messageformatter.md: MessageFormatter
title: 'MessageFormatter::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MessageFormatter::getErrorCode

# msgfmt\_get\_error\_code

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getErrorCode -- msgfmt\_get\_error\_code — Повертає код помилки останньої операції

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

Код помилки є одним із значень UErrorCode. Початкове значення - U\_ZERO\_ERROR.

### Дивіться також

-   [msgfmt\_get\_error\_message()](messageformatter.geterrormessage.md) \- Повертає текст помилки останньої операції
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою

---
navigation:
  - intlcalendar.getdayofweektype.md: '« IntlCalendar::getDayOfWeekType'
  - intlcalendar.geterrormessage.md: 'IntlCalendar::getErrorMessage »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getErrorCode

# intlcal\_get\_error\_code

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getErrorCode -- intlcal\_get\_error\_code — Отримує останній код помилки об'єкта

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public IntlCalendar::getErrorCode(): int|false
```

Процедурний стиль:

```methodsynopsis
intlcal_get_error_code(IntlCalendar $calendar): int|false
```

Повертає числовий код помилки ICU для останнього виклику цього об'єкта (включаючи клонування) або [IntlCalendar](class.intlcalendar.md), вказаний для параметра `calendar` (У версії з процедурним стилем). Це може означати лише попередження (негативний код помилки) або повну відсутність помилки (**`U_ZERO_ERROR`**). Фактичну наявність помилки можна перевірити за допомогою [intl\_is\_failure()](function.intl-is-failure.md)

Недійсні аргументи, виявлені на стороні PHP (до виклику функцій бібліотеки ICU), не записуються для цієї функції.

Останню помилку, яка відбулася за будь-якого виклику функції модуля intl, включаючи помилки ранніх аргументів, можна отримати за допомогою функції [intl\_get\_error\_code()](function.intl-get-error-code.md). Ця функція скидає глобальний код помилки, а чи не код помилки об'єкта.

### Список параметрів

`calendar`

Об'єкт календаря в інтерфейс процедурного стилю.

### Значення, що повертаються

Код помилки ICU, що вказує на успішне виконання, збій чи попередження. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::getErrorCode()**и[IntlCalendar::getErrorMessage()](intlcalendar.geterrormessage.md)**

```php
<?php
ini_set("intl.error_level", E_WARNING);
ini_set("intl.default_locale", "nl");

$intlcal = new IntlGregorianCalendar(2012, 1, 29);
var_dump(
    $intlcal->getErrorCode(),
    $intlcal->getErrorMessage()
);
$intlcal->fieldDifference(-1e100, IntlCalendar::FIELD_SECOND);

var_dump(
    $intlcal->getErrorCode(),
    $intlcal->getErrorMessage()
);
```

Результат виконання наведеного прикладу:

```
int(0)
string(12) "U_ZERO_ERROR"

Warning: IntlCalendar::fieldDifference(): intlcal_field_difference: Call to ICU method has failed in /home/glopes/php/ws/example.php on line 10
int(1)
string(81) "intlcal_field_difference: Call to ICU method has failed: U_ILLEGAL_ARGUMENT_ERROR"
```

### Дивіться також

-   [IntlCalendar::getErrorMessage()](intlcalendar.geterrormessage.md) \- Отримує останнє повідомлення про помилку для об'єкта
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
-   [intl\_error\_name()](function.intl-error-name.md) \- Отримати ім'я помилки за її кодом
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_get\_error\_message()](function.intl-get-error-message.md) \- Отримати опис помилки

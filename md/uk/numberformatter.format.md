---
navigation:
  - numberformatter.formatcurrency.md: '« NumberFormatter::formatCurrency'
  - numberformatter.getattribute.md: 'NumberFormatter::getAttribute »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::format'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::format

# numfmt\_format

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::format -- numfmt\_format — Форматує число

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::format(int|float $num, int $type = NumberFormatter::TYPE_DEFAULT): string|false
```

Процедурний стиль

```methodsynopsis
numfmt_format(NumberFormatter $formatter, int|float $num, int $type = NumberFormatter::TYPE_DEFAULT): string|false
```

Форматує числове значення відповідно до правил засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`num`

Значення форматування. Може бути цілим числом (int) або числом з плаваючою точкою (float), інші типи будуть перетворені на числове значення.

`type`

Використовуваний [тип форматування](class.numberformatter.md#intl.numberformatter-constants.types)Обратите внимание, что константа\*\*`NumberFormatter::TYPE_CURRENCY`\*\* не підтримується; використовуйте замість неї метод [NumberFormatter::formatCurrency()](numberformatter.formatcurrency.md)

### Значення, що повертаються

Повертає рядок, який містить форматоване значення або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** numfmt\_format()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_format($fmt))) {
    report_error("Formatter error");
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

Результат виконання наведеного прикладу:

```
1.234.567,891
```

### Примітки

> **Зауваження** :
> 
> Формати, досягнуті цим способом форматування, не можуть повністю використовувати можливості базової бібліотеки ICU, наприклад форматувати валюту з вузьким символом валюти.
> 
> Для полной поддержки, используйте функцию[msgfmt\_format\_message()](messageformatter.formatmessage.md)

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_format\_currency()](numberformatter.formatcurrency.md) \- Форматує значення валюти
-   [numfmt\_parse()](numberformatter.parse.md) \- Розбирає число
-   [msgfmt\_format\_message()](messageformatter.formatmessage.md) \- Швидко форматує повідомлення

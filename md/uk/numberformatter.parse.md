---
navigation:
  - numberformatter.parsecurrency.md: '« NumberFormatter::parseCurrency'
  - numberformatter.setattribute.md: 'NumberFormatter::setAttribute »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::parse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::parse

# numfmt\_parse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::parse -- numfmt\_parse — Розбирає число

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::parse(string $string, int $type = NumberFormatter::TYPE_DOUBLE, int &$offset = null): int|float|false
```

Процедурний стиль

```methodsynopsis
numfmt_parse(    NumberFormatter $formatter,    string $string,    int $type = NumberFormatter::TYPE_DOUBLE,    int &$offset = null): int|float|false
```

Перетворює рядок на число за правилами засобу форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

`string`

Рядок для аналізу числа.

`type`

Використовуваний [тип форматування](class.numberformatter.md#intl.numberformatter-constants.types)По умолчанию используется\*\*`NumberFormatter::TYPE_DOUBLE`**Обратите внимание, что константа**`NumberFormatter::TYPE_CURRENCY`\*\* не підтримується; скористайтеся замість неї методом [NumberFormatter::parseCurrency()](numberformatter.parsecurrency.md)

`offset`

Зміщення у рядку, з якого починається синтаксичний аналіз. При поверненні це значення міститиме усунення, у якому закінчився синтаксичний аналіз.

### Значення, що повертаються

Повертає значення аналізованого числа чи логічне значення \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**numfmt\_parse()\*\*\*\*

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo numfmt_parse($fmt, $num)."\n";
echo numfmt_parse($fmt, $num, NumberFormatter::TYPE_INT32)."\n";
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$num = "1.234.567,891";
echo $fmt->parse($num)."\n";
echo $fmt->parse($num, NumberFormatter::TYPE_INT32)."\n";
?>
```

Результат виконання наведеного прикладу:

```
1234567.891
1234567
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
-   [numfmt\_format()](numberformatter.format.md) \- Форматує число
-   [numfmt\_parse\_currency()](numberformatter.parsecurrency.md) \- Розбирає номер валюти

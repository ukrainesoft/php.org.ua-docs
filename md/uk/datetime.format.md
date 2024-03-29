---
navigation:
  - datetime.diff.md: '« DateTimeInterface::diff'
  - datetime.getoffset.md: 'DateTimeInterface::getOffset »'
  - index.md: PHP Manual
  - class.datetimeinterface.md: DateTimeInterface
title: 'DateTimeInterface::format'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeInterface::format

# DateTimeImmutable::format

# DateTime::format

# date\_format

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTimeInterface::format -- DateTimeImmutable::format -- DateTime::format -- date\_format — Повертає дату, відформатовану відповідно до переданого формату

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeInterface::format(string $format): string
```

```methodsynopsis
public DateTimeImmutable::format(string $format): string
```

```methodsynopsis
public DateTime::format(string $format): string
```

Процедурний стиль

```methodsynopsis
date_format(DateTimeInterface $object, string $format): string
```

Повертає рядок дати, перетвореної відповідно до переданого формату.

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTime](class.datetime.md), що повертається [date\_create()](function.date-create.md)

`format`

Шаблон результуючого рядка (string) з датою. Дивіться параметри форматування нижче. Також існує кілька [визначених констант дати/часу](class.datetimeinterface.md#datetimeinterface.constants.types), які можна використовувати замість цих параметрів. Наприклад: \*\*`DATE_RSS`\*\*заменяет шаблон`'D, d M Y H:i:s'`

**В параметре`format` розпізнаються такі символи**

| Символ в строке `format` | Опис | Приклад возвращаемого значения |
| --- | --- | --- |
| *День* | \--- | \--- |
| `d` | День місяця, 2 цифри з провідним нулем | Від `01`до`31` |
| `D` | Текстова вистава дня тижня, 3 символи | Від `Mon`до`Sun` |
| `j` | День місяця без ведучого нуля | Від до`31` |
| `l` (маленька 'L') | Повне найменування дня тижня | Від `Sunday`до`Saturday` |
| `N` | Порядковий номер дня тижня відповідно до стандарту ISO 8601 | Від (понеділок) до `7` (Неділя) |
| `S` | Англійський суфікс порядкового числа місяця, 2 символи | `st` `nd` `rd`или`th`. . Застосовують спільно з `j` |
| `w` | Порядковий номер дня тижня | Від (неділя) до`6`(субота) |
| `z` | Порядковий номер дня у році (починаючи з 0) | Від до`365` |
| *Тиждень* | \--- | \--- |
| `W` | Порядковий номер тижня року відповідно до стандарту ISO 8601; тижні починаються з понеділка | Наприклад: `42` (42-й тиждень року) |
| *Місяць* | \--- | \--- |
| `F` | Повне найменування місяця, наприклад January або March | Від `January`до`December` |
| `m` | Порядковий номер місяця з провідним нулем | Від `01`до`12` |
| `M` | Скорочена назва місяця, 3 символи | Від `Jan`до`Dec` |
| `n` | Порядковий номер місяця без провідного нуля | Від до`12` |
| `t` | Кількість днів у вказаному місяці | Від `28`до`31` |
| *Рік* | \--- | \--- |
| `L` | Ознака високосного року | якщо рік високосний, інакше |
| `o` | Номер року відповідно до стандарту ISO 8601. Має те саме значення, що й `Y`крім випадку, коли номер тижня ISO (`W`) належить попередньому чи наступному році; тоді буде використано рік цього тижня. | Приклади: `1999`или`2003` |
| `X` | Розширене повне числове подання року, не менше 4 цифр, `-` для років до нашої ери та `+` для років нашої ери. | Приклади: `-0055` `+0787` `+1999` `+10191` |
| `x` | Розширене повне числове уявлення, якщо потрібно, або стандартне повне числове уявлення, якщо можливо (наприклад, `Y`). Не менш як чотири цифри. Для років до нашої ери вказано префікс `-`. . У років після (і включаючи) `10000` префікс `+` | Приклади: `-0055` `0787` `1999` `+10191` |
| `Y` | Повне числове подання року, не менше 4 цифр, `-` для років до н. | Приклади: `-0055` `0787` `1999` `2003` `10191` |
| `y` | Номер року, 2 цифри | Приклади: `99` `03` |
| *Час* | \--- | \--- |
| `a` | Ante meridiem (лат. «до полудня») або Post meridiem (лат. «після полудня») у нижньому регістрі | `am`или`pm` |
| `A` | Ante meridiem або Post meridiem у верхньому регістрі | `AM`или`PM` |
| `B` | Час у форматі Інтернет-часу (альтернативної системи відліку часу доби) | Від `000`до`999` |
| `g` | Годинник у 12-годинному форматі без провідного нуля | Від до`12` |
| `G` | Годинник у 24-годинному форматі без провідного нуля | Від до`23` |
| `h` | Годинник у 12-годинному форматі з провідним нулем | Від `01`до`12` |
| `H` | Годинник у 24-годинному форматі з провідним нулем | Від `00`до`23` |
| `i` | Хвилини з провідним нулем | Від `00`до`59` |
| `s` | Секунди з провідним нулем | Від `00`до`59` |
| `u` | Мікросекунди. Врахуйте, що функція [date()](function.date.md) завжди повертатиме значення `000000`, т. до. вона приймає цілий (int) параметр, тоді як метод **DateTime::format()** підтримує мікросекунди, якщо об'єкт [DateTime](class.datetime.md) створений із ними. | Наприклад: `654321` |
| `v` | Мілісекунди. Зауваження таке саме, як і для `u` | Приклад: `654` |
| *Часовий пояс* | \--- | \--- |
| `e` | Ідентифікатор часового поясу | Приклади: `UTC` `GMT` `Atlantic/Azores` |
| `I` (Заголовна i) | Ознака літнього часу | якщо дата відповідає літньому часу, в іншому випадку |
| `O` | Різниця з часом за Грінвічем без двокрапки між годинами та хвилинами | Наприклад: `+0200` |
| `P` | Різниця з часом за Грінвічем з двокрапкою між годинами та хвилинами | Наприклад: `+02:00` |
| `p` | Те саме, що і `P`, але повертає`Z` замість `+00:00` (доступний, починаючи з PHP 8.0.0) | Наприклад: `Z`или`+02:00` |
| `T` | Абревіатура часового поясу, якщо відома; в іншому випадку зсув за Грінвічем. | Приклади: `EST` `MDT` `+05` |
| `Z` | Зміщення часового поясу за секунди. Для часових поясів, розташованих на захід від UTC, повертаються негативні числа, а для розташованих на схід від UTC — позитивні. | Від `-43200`до`50400` |
| *Повна дата/час* | \--- | \--- |
| `c` | Дата у форматі стандарту ISO 8601 | 2004-02-12T15:19:21+00:00 |
| `r` | Дата у форматі [» RFC 222](http://www.faqs.org/rfcs/rfc2822) [» RFC 5322](http://www.faqs.org/rfcs/rfc5322) | Наприклад: `Thu, 21 Dec 2000 16:01:07 +0200` |
| `U` | Кількість секунд, що минули з початку Епохи Unix (1 січня 1970 00:00:00 GMT) | Смотрите также[time()](function.time.md) |

Будь-які інші символи, зустрінуті в рядку-шаблоні, будуть виведені в результуючий рядок без змін . `Z` завжди повертає при использовании[gmdate()](function.gmdate.md)

> **Зауваження** :
> 
> Оскільки ця функція приймає як параметр цілочислові (int) мітки часу, символ форматує `u` буде корисним лише при роботі з функцією [date\_format()](function.date-format.md) та користувальницькими мітками часу, створеними функцією [date\_create()](function.date-create.md)

### Значення, що повертаються

Повертає рядок із відформатованою датою у разі успішного виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Додані символи форматування `X`и`x` |
| 8.0.0 | Доданий символ форматування `p` |

### Приклади

**Приклад #1 Приклад використання** DateTimeInterface::format()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$date = new DateTimeImmutable('2000-01-01');
echo $date->format('Y-m-d H:i:s');
?>
```

Процедурний стиль

```php
<?php
$date = date_create('2000-01-01');
echo date_format($date, 'Y-m-d H:i:s');
?>
```

Результат виконання наведеного прикладу:

```
2000-01-01 00:00:00
```

**Приклад #2 Більше прикладів**

```php
<?php
// установка часового пояса по умолчанию.
date_default_timezone_set('UTC');

// сейчас
$date = new DateTimeImmutable();

// Выведет что-то подобное: Wednesday
echo $date->format('l'), "\n";

// Выведет что-то подобное: Wednesday 19th of October 2022 08:40:48 AM
echo $date->format('l jS \o\f F Y h:i:s A'), "\n";

/* Использование констант в параметре format */
// Выведет что-то подобное: Wed, 19 Oct 2022 08:40:48 +0000
echo $date->format(DateTimeInterface::RFC2822), "\n";
?>
```

Можна запобігти розширенню розпізнаного символу в рядку формату, екрануючи його попереднім зворотним слішем. Якщо символ зі зворотним слешем вже утворює спеціальну послідовність, його також може знадобитися екранувати.

**Приклад #3 Екранування символів під час форматування**

```php
<?php
$date = new DateTimeImmutable();

// Выведет что-то подобное: Wednesday the 19th
echo $date->format('l \t\h\e jS');
?>
```

Для форматування дат іншими мовами замість методу **DateTimeInterface::format()** можна використовувати метод [IntlDateFormatter::format()](intldateformatter.format.md)

### Примітки

Цей метод не використовує налаштування локалі. Висновок робиться англійською мовою.

### Дивіться також

-   [date()](function.date.md) \- Форматує тимчасову мітку Unix

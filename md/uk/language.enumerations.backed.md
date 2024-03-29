---
navigation:
  - language.enumerations.basics.md: « Основи перерахувань
  - language.enumerations.methods.md: Методи перерахувань »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Типізовані перерахування
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Типізовані перерахування

За замовчуванням варіанти перерахувань не мають скалярного еквівалента. Це звичайні одноелементні об'єкти. Однак існують випадки, коли варіантам перерахувань потрібно звертатися до бази даних або аналогічного сховища даних, тому корисно мати вбудований скалярний (і, отже, тривіально серіалізується) еквівалент, визначений внутрішньо.

Щоб визначити скалярний еквівалент для перерахувань, користуються наступним синтаксисом:

```php
<?php

enum Suit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}
?>
```

Варіант зі скалярним еквівалентом називається типізованим (Backed Case), оскільки він "підтриманий" більш простим значенням. Перелік, у якого всі варіанти типізовані, називається типизованим перерахуванням (Backed Enum). Типізований перелік може містити лише типізовані варіанти. Чисте перерахування може містити лише чисті варіанти.

Типізований перелік може підтримуватись типами `int`или`string` і такий перелік підтримує лише один тип за раз (тобто не можна об'єднувати `int|string`). Якщо перелік позначений як той, що має скалярний еквівалент, тоді всі варіанти повинні мати певний явно унікальний скалярний еквівалент. Не існує скалярних еквівалентів, що автоматично генеруються (наприклад, послідовних цілих чисел). Типізовані варіанти мають бути унікальними; двом варіантам типізованого перерахування не може належати той самий скалярний еквівалент. Однак константа може належати до варіанта, фактично створюючи псевдонім. Дивіться « [Константи перерахувань](language.enumerations.constants.md) ».

Еквівалентні значення мають бути рядками або рядковими виразами. Константи та постійні вирази не підтримуються. Тобто `1 + 1`разрешено, а`1 + SOME_CONST` - Ні.

Типизовані варіанти мають додаткову доступну тільки для читання властивість `value` - Це значення, задане у визначенні варіанта.

```php
<?php

print Suit::Clubs->value;
// Выведет "C"
?>
```

Щоб властивість `value` залишалося доступним тільки для читання, було заборонено призначати змінну як посилання на неї. Тобто наступний код видасть помилку:

```php
<?php

$suit = Suit::Clubs;
$ref = &$suit->value;
// Error: Cannot acquire reference to property Suit::$value
?>
```

Типізовані перерахування реалізують внутрішній інтерфейс [BackedEnum](class.backedenum.md), який дає два додаткові методи:

-   `from(int|string): self`візьме скаляр і поверне варіант перерахування, якому належить. Якщо варіант, який відповідає варіанту перерахування, не знайдено, метод викине виняток[ValueError](class.valueerror.md). Це переважно корисно тоді, коли вхідний скаляр надійний, а відсутність значення перерахування треба як помилку, зупиняє додаток.
-   `tryFrom(int|string): ?self`візьме скаляр і поверне варіант перерахування, якому належить. Якщо варіант, який відповідає варіанту перерахування, не знайдено, метод поверне`null`. Це в основному корисно тоді, коли вхідний скаляр ненадійний і функція, що викликає, хоче реалізувати свою обробку помилок або логіку значення за умовчанням.

Методи `from()`и`tryFrom()` дотримуються стандартних правил слабкої/суворої типізації. У режимі слабкої типізації допустима передача цілого числа або рядка, система перетворює значення і знайде варіант, який відповідає. Передача числа з плаваючою точкою також працюватиме з примусовим перетворенням. У режимі суворої типізації передача цілого числа метод `from()` у перерахунку з рядковою типізацією (або навпаки) у будь-якому випадку призведе до виключення [TypeError](class.typeerror.md), як і передачі числа з плаваючою точкою. Всі інші типи параметрів викинуть виняток TypeError в обох режимах.

```php
<?php

$record = get_stuff_from_database($id);
print $record['suit'];

$suit =  Suit::from($record['suit']);
// Недопустимые данные выбросят исключение ValueError: "X" is not a valid scalar value for enum "Suit"
print $suit->value;

$suit = Suit::tryFrom('A') ?? Suit::Spades;
// Недопустимые данные возвращают значение null, поэтому вместо этого будет использовано Suit::Spades.
print $suit->value;
?>
```

Ручное определение метода`from()`или`tryFrom()` у типізованих переліках призведе до фатальної помилки.

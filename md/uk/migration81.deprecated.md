---
navigation:
  - migration81.incompatible.md: '« Зміни, що ламають зворотну сумісність'
  - migration81.other-changes.md: Інші зміни »
  - index.md: PHP Manual
  - migration81.md: Міграція з PHP 8.0.x на PHP 8.1.x
title: Застаріла функціональність
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Застаріла функціональність

### Ядро PHP

#### Реализация[Serializable](class.serializable.md)без**\_\_serialize()** і **\_\_unserialize()**

Якщо не потрібна підтримка версій PHP менше 7.4, повинні бути реалізовані лише ці два магічні методи, інакше потрібно реалізувати як методи інтерфейсу, так і магічні методи.

#### Передача\*\*`null`\*\* параметрам вбудованих функцій, які не допускають значення NULL

Не рекомендується передавати значення NULL скалярним параметрам вбудованих функцій. В іншому випадку тепер буде викликане повідомлення. Таке обмеження було введено, щоб краще відповідати роботі функцій користувача, де параметри, що допускають значення NULL, повинні бути для цього явно позначені.

```php
<?php
var_dump(str_contains("foobar", null));
// Deprecated: Passing null to parameter #2 ($needle) of type string
//             is deprecated
?>
```

#### Неявна несумісність перетворення float до int

Тепер потрібно уникати неявного перетворення числа з плаваючою точкою (float) до цілого числа (int), що призводить до втрати точності. Це впливає на ключі масиву (array), оголошення цілих (int) типів у примусовому режимі та операторів, що працюють з цілими числами (int).

```php
<?php
$a = [];
$a[15.5]; // устарело, поскольку значение ключа теряет компонент 0.5
$a[15.0]; // работает, так как 15.0 == 15
?>
```

#### Виклик static-елемента у трейтах

Виклик static-методу або доступ до static-властивості безпосередньо в трейті застарів. До статичних методів та властивостей слід звертатися лише у класі, який використовує трейт.

#### Возврат не массива (array) из**\_\_sleep()**

Возвращаемое значение[\_\_sleep()](language.oop5.magic.md#object.sleep), що не є масивом, тепер згенерує повідомлення.

#### Повернення значення за посиланням функції void

```php
<?php
function &test(): void {}
?>
```

Така функція збиває з пантелику, тому тепер видасть наступний **`E_NOTICE`** `Only variable references should be returned by reference` (За посиланням повинні повертатися лише посилання змінні).

#### Автовивификация из\*\*`false`\*\*

Автовівіфікація - це створення нового масиву (array) при додаванні нового значення. Автовівіфікація заборонена для скалярних значень, проте **`false`** був винятком. Тепер така поведінка застаріла.

```php
<?php
$arr = false;
$arr[] = 2;   // устарело
?>
```

> **Зауваження** :
> 
> Автовивификация из\*\*`null`\*\* та невизначеного значення як і раніше дозволена:
> 
> ```php
> <?php
> // З невизначеного значення
> $arr[] = 'якесь значення';
> $arr['doesNotExist'][] = 2;
> // З null
> $ arr = null;
> $arr[] = 2;
> ?>
> ```

### ctype

#### Перевірка нерядкових аргументів

Передача нерядкового аргументу застаріла. У майбутньому аргумент інтерпретуватиметься як рядок замість коду ASCII. Залежно від передбачуваної поведінки, аргумент повинен бути приведений до рядка (string) явним чином або через виклик [chr()](function.chr.md). Ця зміна стосується всіх функцій `ctype_*()`

### Date

Функції [date\_sunrise()](function.date-sunrise.md) і [date\_sunset()](function.date-sunset.md)устарели в пользу[date\_sun\_info()](function.date-sun-info.md)

Функция[strptime()](function.strptime.md) застаріла. Замість неї використовуйте [date\_parse\_from\_format()](function.date-parse-from-format.md) (для синтаксичного аналізу, що не залежить від мовного стандарту) або [IntlDateFormatter::parse()](intldateformatter.parse.md) (Для синтаксичного аналізу, що залежить від мовного стандарту).

Функция[strftime()](function.strftime.md) і [gmstrftime()](function.gmstrftime.md)устарели. Используйте вместо них функцию[date()](function.date.md) (для форматування, що не залежить від мовного стандарту) або метод [IntlDateFormatter::format()](intldateformatter.format.md) (Для форматування, що залежить від мовного стандарту).

### Фільтр

Фільтри \*\*`FILTER_SANITIZE_STRING`** і **`FILTER_SANITIZE_STRIPPED`\*\*устарели.

INI-директива[filter.default](filter.configuration.md#ini.filter.default)устарела.

### GD

Параметр`num_points` функції [imagepolygon()](function.imagepolygon.md) [imageopenpolygon()](function.imageopenpolygon.md) і [imagefilledpolygon()](function.imagefilledpolygon.md)устарел.

### Хешування

Функції [mhash()](function.mhash.md) [mhash\_keygen\_s2k()](function.mhash-keygen-s2k.md) [mhash\_count()](function.mhash-count.md) [mhash\_get\_block\_size()](function.mhash-get-block-size.md) і [mhash\_get\_hash\_name()](function.mhash-get-hash-name.md) застаріли. Замість них використовуйте функції `hash_*()`

### IMAP

Константа\*\*`NIL`\*\* застаріла. Замість неї використовуйте

### Intl

Виклик [IntlCalendar::roll()](intlcalendar.roll.md)с логическим значением (bool) устарел. Используйте и`-1` замість \*\*`true`** і **`false`\*\*соответственно.

### Багатобайтові рядки

Виклик [mb\_check\_encoding()](function.mb-check-encoding.md) без жодних аргументів застарів.

### MySQLi

Властивість mysqli\_driver::$driver\_version застаріло. Воно було неактуальним, використовуйте замість нього **`PHP_VERSION_ID`**

Виклик методу [mysqli::get\_client\_info()](mysqli.get-client-info.md) або [mysqli\_get\_client\_info()](mysqli.get-client-info.md) з аргументом `mysqli`устарел. Используйте[mysqli\_get\_client\_info()](mysqli.get-client-info.md) без жодних аргументів, щоб отримати інформацію про версію клієнтської бібліотеки.

Метод[mysqli::init()](mysqli.init.md) застарів. Замініть дзвінки **parent::init()**на**parent::\_\_construct()**

### OCI8

INI-директива[oci8.old\_oci\_close\_semantics](oci8.configuration.md#ini.oci8.old-oci-close-semantics)устарела.

### ODBC

Функция[odbc\_result\_all()](function.odbc-result-all.md)устарела.

### PDO

Режим вибірки \*\*`PDO::FETCH_SERIALIZE`\*\*устарел.

### PgSQL

Функциям`pgsql_*()` Тепер потрібно явно передавати параметр connection.

### SOAP

Параметр`ssl_method`в[SoapClient::\_\_construct()](soapclient.construct.md)устарел в пользу параметров контекста потока SSL.

### Стандартні функції

Виклик [key()](function.key.md) [current()](function.current.md) [next()](function.next.md) [prev()](function.prev.md) [reset()](function.reset.md) або [end()](function.end.md) з об'єктами (object) застарів. Або спочатку перетворіть об'єкт (object) на масив (array) за допомогою функції [get\_mangled\_object\_vars()](function.get-mangled-object-vars.md), або використовуйте методи, що надаються класом, що реалізує інтерфейс [Iterator](class.iterator.md), наПриклад,[ArrayIterator](class.arrayiterator.md)

INI-директива[auto\_detect\_line\_endings](filesystem.configuration.md#ini.auto-detect-line-endings) застаріла. При необхідності обробіть розриви рядків `"\r"`вручную.

Константи **`FILE_BINARY`** і **`FILE_TEXT`** застаріли. Вони ніколи не мали сенсу.

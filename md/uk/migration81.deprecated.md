---
navigation:
  - migration81.incompatible.html: '« Зміни, що ламають зворотну сумісність'
  - migration81.other-changes.html: Другие изменения »
  - index.html: PHP Manual
  - migration81.html: Миграция с PHP 8.0.x на PHP 8.1.x
title: Застаріла функціональність
---
## Застаріла функціональність

### Ядро PHP

#### Реалізація [Serializable](class.serializable.html) без **serialize()** і **unserialize()**

Якщо не потрібна підтримка версій PHP менше 7.4, повинні бути реалізовані лише ці два магічні методи, інакше потрібно реалізувати як методи інтерфейсу, так і магічні методи.

#### Передача **`null`** параметрам вбудованих функцій, які не допускають значення NULL

Не рекомендується передавати значення NULL скалярним параметрам вбудованих функцій. В іншому випадку тепер буде викликане повідомлення. Таке обмеження було введено, щоб краще відповідати роботі функцій користувача, де параметри, що допускають значення NULL, повинні бути для цього явно позначені.

```php
<?php
var_dump(str_contains("foobar", null));
// Deprecated: Passing null to parameter #2 ($needle) of type string
//             is deprecated
?>
```

#### Неявна несумісність перетворення float до int

Тепер потрібно уникати неявного перетворення числа з плаваючою точкою (float) до цілого числа (int), що призводить до втрати точності. Це впливає на ключі масиву (array), оголошення цілих (int) типів у примусовому режимі та операторів, що працюють з цілими числами (int).

```php
<?php
$a = [];
$a[15.5]; // устарело, поскольку значение ключа теряет компонент 0.5
$a[15.0]; // работает, так как 15.0 == 15
?>
```

#### Виклик staticелемента у трейтах

Виклик staticметоду або доступ до staticвластивості безпосередньо в трейті застарів. До статичних методів та властивостей слід звертатися лише у класі, який використовує трейт.

#### Повернення не масиву (array) з **sleep()**

Значення, що повертається [sleep()](language.oop5.magic.html#object.sleep), що не є масивом, тепер згенерує повідомлення.

#### Повернення значення за посиланням функції void

```php
<?php
function &test(): void {}
?>
```

Така функція збиває з пантелику, тому тепер видасть наступний **`E_NOTICE`** `Only variable references should be returned by reference` (За посиланням повинні повертатися лише посилання змінні).

#### Автовівіфікація з **`false`**

Автовівіфікація - це створення нового масиву (array) при додаванні нового значення. Автовівіфікація заборонена для скалярних значень, проте **`false`** був винятком. Тепер така поведінка застаріла.

```php
<?php
$arr = false;
$arr[] = 2;   // устарело
?>
```

> **Зауваження**
> 
> Автовівіфікація з **`null`** та невизначеного значення як і раніше дозволена:
> 
> ```php
> <?php
> // Из неопределённого значения
> $arr[] = 'какое-то значение';
> $arr['doesNotExist'][] = 2;
> // Из null
> $arr = null;
> $arr[] = 2;
> ?>
> ```

### ctype

#### Перевірка нерядкових аргументів

Передача нерядкового аргументу застаріла. У майбутньому аргумент інтерпретуватиметься як рядок замість коду ASCII. Залежно від передбачуваної поведінки аргумент має бути приведений до рядка (string) явно або через виклик [chr()](function.chr.html). Ця зміна стосується всіх функцій `ctype_*()`

### Date

Функції [datesunrise()](function.date-sunrise.html) і [datesunset()](function.date-sunset.html) застаріли на користь [datesuninfo()](function.date-sun-info.html)

Функція [strptime()](function.strptime.html) застаріла. Замість неї використовуйте [dateparsefromformat()](function.date-parse-from-format.html) (для синтаксичного аналізу, що не залежить від мовного стандарту) або [IntlDateFormatter::parse()](intldateformatter.parse.html) (Для синтаксичного аналізу, що залежить від мовного стандарту).

Функція [strftime()](function.strftime.html) і [gmstrftime()](function.gmstrftime.html) застаріли. Використовуйте замість них функцію [date()](function.date.html) (для форматування, що не залежить від мовного стандарту) або метод [IntlDateFormatter::format()](intldateformatter.format.html) (Для форматування, що залежить від мовного стандарту).

### Фільтр

Фільтри **`FILTER_SANITIZE_STRING`** і **`FILTER_SANITIZE_STRIPPED`** застаріли.

INI-директива [filter.default](filter.configuration.html#ini.filter.default) застаріла.

### ДД

Параметр `num_points` функції [imagepolygon()](function.imagepolygon.html) [imageopenpolygon()](function.imageopenpolygon.html) і [imagefilledpolygon()](function.imagefilledpolygon.html) застарів.

### Хешування

Функції [mhash()](function.mhash.html) [mhashkeygens2k()](function.mhash-keygen-s2k.html) [mhashcount()](function.mhash-count.html) [mhashgetblocksize()](function.mhash-get-block-size.html) і [mhashgethashname()](function.mhash-get-hash-name.html) застаріли. Замість них використовуйте функції `hash_*()`

### IMAP

Константа **`NIL`** застаріла. Замість неї використовуйте `0`

### Intl

Виклик [IntlCalendar::roll()](intlcalendar.roll.html) із логічним значенням (bool) застарів. Використовуйте `1` і `-1` замість **`true`** і **`false`** відповідно.

### Багатобайтові рядки

Виклик [мбcheckencoding()](function.mb-check-encoding.html) без жодних аргументів застарів.

### MySQLi

Властивість mysqlidriver::$driverversion застаріло. Воно було неактуальним, використовуйте замість нього **`PHP_VERSION_ID`**

Виклик методу [mysqli::getclientinfo()](mysqli.get-client-info.html) або [mysqligetclientinfo()](mysqli.get-client-info.html) з аргументом `mysqli` застарів. Використовуйте [mysqligetclientinfo()](mysqli.get-client-info.html) без жодних аргументів, щоб отримати інформацію про версію клієнтської бібліотеки.

Метод [mysqli::init()](mysqli.init.html) застарів. Замініть дзвінки **parent::init()** на **parent::construct()**

### OCI8

INI-директива [oci8.oldociclosesemantics](oci8.configuration.html#ini.oci8.old-oci-close-semantics) застаріла.

### ODBC

Функція [odbcresultall()](function.odbc-result-all.html) застаріла.

### PDO

Режим вибірки **`PDO::FETCH_SERIALIZE`** застарів.

### PgSQL

функцій `pgsql_*()` Тепер потрібно явно передавати параметр connection.

### SOAP

Параметр `ssl_method` в [SoapClient::construct()](soapclient.construct.html) застарів на користь параметрів контексту потоку SSL.

### Стандартні функції

Виклик [key()](function.key.html) [current()](function.current.html) [next()](function.next.html) [prev()](function.prev.html) [reset()](function.reset.html) або [end()](function.end.html) з об'єктами (object) застарів. Використовуйте ці функції на об'єкті через [getmangledobjectvars()](function.get-mangled-object-vars.html), або через [ArrayIterator](class.arrayiterator.html)

INI-директива [autodetectlineendings](filesystem.configuration.html#ini.auto-detect-line-endings) застаріла. При необхідності обробіть розриви рядків `"\r"` вручну.

Константи **`FILE_BINARY`** і **`FILE_TEXT`** застаріли. Вони ніколи не мали сенсу.

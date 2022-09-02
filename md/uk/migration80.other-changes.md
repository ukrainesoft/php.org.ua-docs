---
navigation:
  - migration80.deprecated.md: '« Функціональність, оголошена застарілою в PHP 8.0.x'
  - migration74.md: Миграция с PHP 7.3.x на PHP 7.4.x »
  - index.md: PHP Manual
  - migration80.md: Миграция с PHP 7.4.x на PHP 8.0.x
title: Інші зміни
---
## Інші зміни

### Зміни у модулях SAPI

#### Apache2Handler

Модуль PHP був перейменований з `php7_module` в `php_module`

### Змінені функції

#### Reflection

Результати [ReflectionClass::getConstants()](reflectionclass.getconstants.md) і [ReflectionClass::getReflectionConstants()](reflectionclass.getreflectionconstants.md) тепер можна фільтрувати за допомогою нового параметра `filter`. Додано три нові константи для роботи з ним:

-   **`ReflectionClassConstant::IS_PUBLIC`**
-   **`ReflectionClassConstant::IS_PROTECTED`**
-   **`ReflectionClassConstant::IS_PRIVATE`**

#### Стандартні функції

Математичні функції [abs()](function.abs.md) [ceil()](function.ceil.md) [floor()](function.floor.md) і [round()](function.round.md) тепер правильно враховують [оголошення`strict_type`](language.types.declarations.md#language.types.declarations.strict). Раніше вони наводили перший аргумент до числового значення навіть у режимі суворої типізації.

#### Zip

-   Методи [ZipArchive::addGlob()](ziparchive.addglob.md) і [ZipArchive::addPattern()](ziparchive.addpattern.md) набувають нових значень у масиві параметрів `options`
    
    -   `flags`
    -   `comp_method`
    -   `comp_flags`
    -   `env_method`
    -   `enc_password`
-   У методів [ZipArchive::addEmptyDir()](ziparchive.addemptydir.md) [ZipArchive::addFile()](ziparchive.addfile.md) і [ZipArchive::addFromString()](ziparchive.addfromstring.md) додано новий параметр `flags`. За допомогою нього можна керувати кодуванням імені (**`ZipArchive::FL_ENC_*`**) та заміною запису (**`ZipArchive::FL_OVERWRITE`**
    
-   [ZipArchive::extractTo()](ziparchive.extractto.md) Тепер відновлює час модифікації файлу.
    

### Інші зміни у модулях

#### CURL

-   Для роботи модуля CURL тепер потрібно щонайменше libcurl 7.29.0.
    
-   Застарілий параметр `version` функції [curlversion()](function.curl-version.md) був видалений.
    

#### дата і час

[DatePeriod](class.dateperiod.md) тепер реалізує [IteratorAggregate](class.iteratoraggregate.md) (замість [Traversable](class.traversable.md)

#### DOM

[DOMNamedNodeMap](class.domnamednodemap.md) і [DOMNodeList](class.domnodelist.md) тепер реалізують [IteratorAggregate](class.iteratoraggregate.md) (замість [Traversable](class.traversable.md)

#### Intl

[IntlBreakIterator](class.intlbreakiterator.md) і [ResourceBundle](class.resourcebundle.md) тепер реалізують [IteratorAggregate](class.iteratoraggregate.md) (замість [Traversable](class.traversable.md)

#### Enchant

Модуль enchant тепер використовує libenchant-2 за замовчуванням, якщо це можливо. libenchant версії 1 все ще підтримується, але застарілий і може бути вилучений у майбутньому.

#### ДД

-   Параметр `num_points` для [imagepolygon()](function.imagepolygon.md) [imageopenpolygon()](function.imageopenpolygon.md) і [imagefilledpolygon()](function.imagefilledpolygon.md) тепер необов'язковий, тобто ці функції можуть бути викликані за допомогою трьох або чотирьох параметрів. Якщо параметр опущено, він розраховується як `count($points)/2`
    
-   Додана функція [imagegetinterpolation()](function.imagegetinterpolation.md) для одержання поточного методу інтерполяції.
    

#### JSON

Модуль JSON більше не можна відключити, тепер він є невід'ємною частиною будь-якої збірки PHP, як і модуль date.

#### MBString

Таблиці даних Unicode оновлено до версії 13.0.0.

#### PDO

[PDOStatement](class.pdostatement.md) тепер реалізує [IteratorAggregate](class.iteratoraggregate.md) (замість [Traversable](class.traversable.md)

#### LibXML

Мінімальна необхідна версія libxml – 2.9.0. Це означає, що завантаження зовнішніх об'єктів за замовчуванням тепер вимкнуто і тому не потрібні додаткові кроки для захисту від XXE-атак.

#### MySQLi / PDO MySQL

-   Якщо mysqlnd не використовується (це варіант за промовчанням і рекомендується), мінімальна підтримувана версія libmysqlclient тепер 5.5.
    
-   [mysqliresult](class.mysqli-result.md) тепер реалізує [IteratorAggregate](class.iteratoraggregate.md) (замість [Traversable](class.traversable.md)
    

#### PGSQL / PDO PGSQL

Для модулів PGSQL та PDO PGSQL тепер потрібно як мінімум libpq 9.1.

#### Readline

Виклик [readlinecompletionfunction()](function.readline-completion-function.md) перед запуском інтерактивної підказки (наприклад, [autoprependfile](ini.core.md#ini.auto-prepend-file)) тепер скасовує функцію завершення інтерактивної підказки за замовчуванням. Раніше [readlinecompletionfunction()](function.readline-completion-function.md) працювала лише під час виклику після запуску інтерактивної підказки.

#### SimpleXML

[SimpleXMLElement](class.simplexmlelement.md) тепер реалізує [RecursiveIterator](class.recursiveiterator.md) і включає функціонал [SimpleXMLIterator](class.simplexmliterator.md). . [SimpleXMLIterator](class.simplexmliterator.md) є порожнім розширенням [SimpleXMLElement](class.simplexmlelement.md)

### Зміни в обробці INI-файлів

-   com.dotnetversion - це нова INI-директива для вибору версії платформи .NET, яка використовуватиметься для об'єктів [dotnet](class.dotnet.md)
    
-   zend.exceptionstringparammaxlen - це нова INI-директива для встановлення максимальної довжини рядка в аргументі рядкового трасування стека.
    

### EBCDIC

Цілі EBCDIC більше не підтримуються, хоча малоймовірно, що вони й досі працювали.

### Продуктивність

-   Компілятор Just-In-Time (JIT) був доданий у модуль opcache.
    
-   [arrayslice()](function.array-slice.md) в масиві без відстані між елементами більше не скануватиме весь масив, щоб знайти початкове зміщення. Це може значно скоротити час виконання функції з великими зсувами та малою довжиною.
    
-   [strtolower()](function.strtolower.md) тепер використовує реалізацію SIMD у локалі `"C"` **`LC_CTYPE`** (яка використовується за замовчуванням).

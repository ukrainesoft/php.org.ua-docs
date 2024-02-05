---
navigation:
  - migration81.constants.md: « Нові глобальні константи
  - migration81.deprecated.md: Застаріла функціональність »
  - index.md: PHP Manual
  - migration81.md: Міграція з PHP 8.0.x на PHP 8.1.x
title: 'Зміни, що ламають зворотну сумісність'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Зміни, що ламають зворотну сумісність

### Ядро PHP

#### Обмеження доступу до $GLOBALS

Доступ к массиву[$GLOBALS](reserved.variables.globals.md) тепер має низку обмежень. Читання та запис окремих елементів масиву, наприклад, `$GLOBALS['var']`, як і раніше працює. Читання всього масиву [$GLOBALS](reserved.variables.globals.md) також підтримується. Однак операції, пов'язані зі зміною всього [$GLOBALS](reserved.variables.globals.md), заборонено. Наприклад, `array_pop($GLOBALS)` призведе до помилки.

#### Використання static-змінних у успадкованих методах

Коли метод, який використовує статичні змінні, успадковується (але не перевизначається), успадкований метод тепер використовуватиме статичні змінні разом із батьківським методом.

```php
<?php
class A {
    public static function counter() {
        static $counter = 0;
        $counter++;
        return $counter;
    }
}
class B extends A {}
var_dump(A::counter()); // int(1)
var_dump(A::counter()); // int(2)
var_dump(B::counter()); // int(3), ранее было int(1)
var_dump(B::counter()); // int(4), ранее было int(2)
?>
```

Це означає, що статичні змінні в методах тепер поводяться так само, як і статичні властивості.

#### Необов'язкові параметри, вказані перед обов'язковими параметрами

[Необов'язковий параметр](functions.arguments.md#functions.arguments.default), вказаний перед обов'язковими параметрами, тепер завжди обробляється як обов'язковий навіть при виклику з використанням [іменованих аргументів](functions.arguments.md#functions.named-arguments). Починаючи з PHP 8.0.0, але до PHP 8.1.0, наведений нижче код видає попередження про старіння визначення, але успішно виконується під час виклику. Починаючи з PHP 8.1.0, видається помилка класу [ArgumentCountError](class.argumentcounterror.md), як це було б під час виклику з позиційними аргументами.

```php
<?php
function makeyogurt($container = "миску", $flavour)
{
    return "Готовим $container с $flavour йогуртом.\n";
}
try
{
    echo makeyogurt(flavour: "малиновым");
}
catch (Error $e)
{
    echo get_class($e), ' - ', $e->getMessage(), "\n";
}
?>
```

Результат виконання наведеного прикладу в PHP 8.0:

```
Deprecated: Required parameter $flavour follows optional parameter $container
 in example.php on line 3
Готовим миску с малиновым йогуртом.
```

Результат виконання наведеного прикладу в PHP 8.1:

```
Deprecated: Optional parameter $container declared before required parameter
 $flavour is implicitly treated as a required parameter in example.php on line 3
ArgumentCountError - makeyogurt(): Argument #1 ($container) not passed
```

Обратите внимание, что значение по умолчанию\*\*`null`\*\* може використовуватися перед обов'язковими параметрами для вказівки [типу, що припускає значення null](language.types.declarations.md#language.types.declarations.nullable)Але цей параметр все одно буде обов'язковим.

#### Сумісність типу значення, що повертається з внутрішніми класами

Більшість неостаточних внутрішніх методів тепер потребують перевизначальних методів для оголошення сумісного типу, що повертається, в іншому випадку під час перевірки успадкування видається повідомлення про старіння можливості. У випадку, якщо тип значення, що повертається, не може бути оголошений для методу перевизначення через проблеми сумісності версій PHP, можна додати атрибут [ReturnTypeWillChange](class.returntypewillchange.md), щоб заглушити повідомлення про старіння.

#### Нові ключові слова

`readonly` тепер є ключовим словом. Однак, його можна використовувати як ім'я функції.

`never` тепер є зарезервованим словом, тому його не можна використовувати для назви класу, інтерфейсу або трейту, а також заборонено використовувати у просторах імен.

### Перехід від ресурсів до об'єктів

Декілька ресурсів ([resource](language.types.resource.md)) тепер представлені як об'єкти (object). Перевірки значення, що повертається з використанням функції [is\_resource()](function.is-resource.md) слід замінити перевірками на **`false`**

-   Функції [FileInfo](book.fileinfo.md)тепер приймають та повертають об'єкти[finfo](class.finfo.md)замість ресурсів ([resource](language.types.resource.md) `fileinfo`
    
-   Функції [FTP](book.ftp.md)тепер приймають та повертають об'єкти[FTP\\Connection](class.ftp-connection.md)замість ресурсів ([resource](language.types.resource.md) `ftp`
    
-   Функції [IMAP](book.imap.md)тепер приймають та повертають об'єкти[IMAP\\Connection](class.imap-connection.md)замість ресурсів ([resource](language.types.resource.md) `imap`
    
-   The[LDAP](book.ldap.md)тепер приймають та повертають об'єкти[LDAP\\Connection](class.ldap-connection.md)замість ресурсів ([resource](language.types.resource.md) `ldap link`
    
-   Функції [LDAP](book.ldap.md)тепер приймають та повертають об'єкти[LDAP\\Result](class.ldap-result.md)замість ресурсів ([resource](language.types.resource.md) `ldap result`
    
-   Функції [LDAP](book.ldap.md)тепер приймають та повертають об'єкти[LDAP\\ResultEntry](class.ldap-result-entry.md)замість ресурсів ([resource](language.types.resource.md) `ldap result entry`
    
-   Функції [PgSQL](book.pgsql.md)тепер приймають та повертають об'єкти[PgSql\\Connection](class.pgsql-connection.md)замість ресурсів ([resource](language.types.resource.md) `pgsql link`
    
-   Функції [PgSQL](book.pgsql.md)тепер приймають та повертають об'єкти[PgSql\\Result](class.pgsql-result.md)замість ресурсів ([resource](language.types.resource.md) `pgsql result`
    
-   Функції [PgSQL](book.pgsql.md)тепер приймають та повертають об'єкти[PgSql\\Lob](class.pgsql-lob.md)замість ресурсів ([resource](language.types.resource.md) `pgsql large object`
    
-   Функції [PSpell](book.pspell.md)тепер приймають та повертають об'єкти[PSpell\\Dictionary](class.pspell-dictionary.md)замість ресурсів ([resource](language.types.resource.md) `pspell`
    
-   Функції [PSpell](book.pspell.md)тепер приймають та повертають об'єкти[PSpell\\Config](class.pspell-config.md)замість ресурсів ([resource](language.types.resource.md) `pspell config`
    

### MySQLi

Функції [mysqli\_fetch\_fields()](mysqli-result.fetch-fields.md) і [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) тепер завжди повертають у властивості max\_length. Це значення можна обчислити, перебираючи набір результатів та вибираючи максимальну довжину. Такий алгоритм раніше використовував PHP.

Опция\*\*`MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH`\*\* більше немає сенсу.

Опция\*\*`MYSQLI_STORE_RESULT_COPY_DATA`\*\* більше немає сенсу. Передача будь-якого значення параметр `mode`метода[mysqli::store\_result()](mysqli.store-result.md) більше немає сенсу.

[mysqli::connect()](function.mysqli-connect.md) тепер повертає **`true`** замість **`null`** у разі успішного виконання.

Режим обробки помилок за умовчанням було змінено з "silent" на "exceptions". Дивіться сторінку [Режими обробки помилок MySQLi](mysqli-driver.report-mode.md) для отримання додаткових відомостей про те, що це спричиняє і як явно встановити цей атрибут. Щоб відновити попередню поведінку, використовуйте: `mysqli_report(MYSQLI_REPORT_OFF);`

Класи, що розширюють [mysqli\_stmt::execute()](mysqli-stmt.execute.md), тепер потрібно вказати додатковий необов'язковий параметр.

### MySQLnd

INI-директива[mysqlnd.fetch\_data\_copy](mysqlnd.config.md#ini.mysqlnd.fetch_data_copy) було видалено. Це не повинно призводити до видимих ​​для користувача змін у поведінці.

### OpenSSL

Секретні ключі EC тепер експортуватимуться у форматі PKCS#8, а не у традиційному форматі, як і всі інші ключі.

Функції [openssl\_pkcs7\_encrypt()](function.openssl-pkcs7-encrypt.md) і [openssl\_cms\_encrypt()](function.openssl-cms-encrypt.md) тепер за замовчуванням використовують шифр AES-128-CBC, а чи не RC2-40. Шифр RC2-40 вважається небезпечним і не включений за промовчанням у OpenSSL 3.

### Об'єкти даних PHP

Атрибут\*\*`PDO::ATTR_STRINGIFY_FETCHES`\*\* тепер перетворює логічні значення (bool) на `"0"`или`"1"`. Раніше логічні значення (bool) були строковими.

Виклик [PDOStatement::bindColumn()](pdostatement.bindcolumn.md)с\*\*`PDO::PARAM_LOB`\*\* тепер буде постійно пов'язувати результат потоку, якщо **`PDO::ATTR_STRINGIFY_FETCHES`** не увімкнуто. Раніше результатом був або потік, або рядок в залежності від драйвера бази даних, що використовується, і часу виконання прив'язки.

#### Драйвер MySQL

Цілі числа та числа з плаваючою комою у наборах результатів тепер повертатимуться з використанням власних типів PHP замість рядків (string) при використанні емульованих підготовлених операторів. Це відповідає поведінці своїх підготовлених операторів. Попередню поведінку можна відновити, увімкнувши опцію **`PDO::ATTR_STRINGIFY_FETCHES`**

#### Драйвер SQLite

Цілі числа та числа з плаваючою комою у наборах результатів тепер повертатимуться з використанням власних типів PHP. Попередню поведінку можна відновити, увімкнувши опцію **`PDO::ATTR_STRINGIFY_FETCHES`**

### Phar

Щоб відповідати інтерфейсу [ArrayAccess](class.arrayaccess.md) [Phar::offsetUnset()](phar.offsetunset.md) і [PharData::offsetUnset()](phardata.offsetunset.md) більше повертають логічне значення (bool).

### Стандартні функції

[version\_compare()](function.version-compare.md) більше не приймає недокументованих скорочень операторів.

Функції [htmlspecialchars()](function.mdspecialchars.md) [htmlentities()](function.mdentities.md) [htmlspecialchars\_decode()](function.mdspecialchars-decode.md) [html\_entity\_decode()](function.md-entity-decode.md) і [get\_html\_translation\_table()](function.get-html-translation-table.md)теперь по умолчанию используют`ENT_QUOTES | ENT_SUBSTITUTE` замість **`ENT_COMPAT`**. Це означає, що тепер `'` екранується в `&#039;`. Крім того, у разі неправильного UTF-8 замість порожнього рядка буде повернено заміщувальний символ Unicode.

[debug\_zval\_dump()](function.debug-zval-dump.md) тепер виводить refcount оболонок посилань з їх refcount, замість того, щоб просто додавати `&` до значення. Це більш точно моделює еталонну виставу, починаючи з PHP 7.0.

[debug\_zval\_dump()](function.debug-zval-dump.md) тепер виводить `interned` замість фіктивного refcount для інтернованих рядків та незмінних масивів.

### Стандартна бібліотека PHP (SPL)

[SplFixedArray](class.splfixedarray.md) тепер буде закодовано в JSON як масив (array).

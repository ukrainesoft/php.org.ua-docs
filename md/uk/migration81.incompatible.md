Зміни, що ламають зворотну сумісність

-   [« Новые глобальные константы](migration81.constants.html)
    
-   [Устаревшая функциональность »](migration81.deprecated.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 8.0.x на PHP 8.1.x](migration81.html)
    
-   Зміни, що ламають зворотну сумісність
    

## Зміни, що ламають зворотну сумісність

### Ядро PHP

#### Обмеження доступу до $GLOBALS

Доступ до масиву [$GLOBALS](reserved.variables.globals.html) тепер має низку обмежень. Читання та запис окремих елементів масиву, наприклад, `$GLOBALS['var']`, як і раніше працює. Читання всього масиву [$GLOBALS](reserved.variables.globals.html) також підтримується. Однак операції, пов'язані зі зміною всього [$GLOBALS](reserved.variables.globals.html), заборонено. Наприклад, `array_pop($GLOBALS)` призведе до помилки.

#### Використання staticзмінних у успадкованих методах

Коли метод, який використовує статичні змінні, успадковується (але не перевизначається), успадкований метод тепер використовуватиме статичні змінні разом із батьківським методом.

```php
<?php
class A {
    public static function counter() {
        static $counter = 0;
        $counter++;
        return $counter;
    }
}
class B extends A {}
var_dump(A::counter()); // int(1)
var_dump(A::counter()); // int(2)
var_dump(B::counter()); // int(3), ранее было int(1)
var_dump(B::counter()); // int(4), ранее было int(2)
?>
```

Це означає, що статичні змінні в методах тепер поводяться так само, як і статичні властивості.

#### Необов'язкові параметри, вказані перед обов'язковими параметрами

[Необов'язковий параметр](functions.arguments.html#functions.arguments.default), вказаний перед обов'язковими параметрами, тепер завжди обробляється як обов'язковий навіть при виклику з використанням [именованных аргументов](functions.arguments.html#functions.named-arguments). Починаючи з PHP 8.0.0, але до PHP 8.1.0, наведений нижче код видає попередження про старіння визначення, але успішно виконується під час виклику. Починаючи з PHP 8.1.0, видається помилка класу [ArgumentCountError](class.argumentcounterror.html), як це було б під час виклику з позиційними аргументами.

```php
<?php
function makeyogurt($container = "миску", $flavour)
{
    return "Готовим $container с $flavour йогуртом.\n";
}
try
{
    echo makeyogurt(flavour: "малиновым");
}
catch (Error $e)
{
    echo get_class($e), ' - ', $e->getMessage(), "\n";
}
?>
```

Результат виконання цього прикладу в PHP 8.0:

```
Deprecated: Required parameter $flavour follows optional parameter $container
 in example.php on line 3
Готовим миску с малиновым йогуртом.
```

Результат виконання цього прикладу в PHP 8.1:

```
Deprecated: Optional parameter $container declared before required parameter
 $flavour is implicitly treated as a required parameter in example.php on line 3
ArgumentCountError - makeyogurt(): Argument #1 ($container) not passed
```

Зверніть увагу, що значення за замовчуванням **`null`** може використовуватися перед обов'язковими параметрами для вказівки [типа, допускающего значение null](language.types.declarations.html#language.types.declarations.nullable)Але цей параметр все одно буде обов'язковим.

#### Сумісність типу значення, що повертається, з внутрішніми класами

Більшість неостаточних внутрішніх методів тепер потребують перевизначальних методів для оголошення сумісного типу, що повертається, в іншому випадку під час перевірки успадкування видається повідомлення про старіння можливості. У випадку, якщо тип значення, що повертається, не може бути оголошений для методу перевизначення через проблеми сумісності версій PHP, можна додати атрибут `#[ReturnTypeWillChange]`, щоб заглушити повідомлення про старіння.

#### Нові ключові слова

`readonly` тепер є ключовим словом. Однак, його можна використовувати як ім'я функції.

`never` тепер є зарезервованим словом, тому його не можна використовувати для назви класу, інтерфейсу чи трейту, а також заборонено використовувати у просторах імен.

### Перехід від ресурсів до об'єктів

Декілька ресурсів ([resource](language.types.resource.html)) тепер представлені як об'єкти (object). Перевірки значення, що повертається з використанням функції [ісresource()](function.is-resource.html) слід замінити перевірками на **`false`**

-   Функції [FileInfo](book.fileinfo.html) тепер приймають та повертають об'єкти [finfo](class.finfo.html) замість ресурсів ([resource](language.types.resource.html) `fileinfo`
    
-   Функції [FTP](book.ftp.html) тепер приймають та повертають об'єкти [FTPConnection](class.ftp-connection.html) замість ресурсів ([resource](language.types.resource.html) `ftp`
    
-   Функції [IMAP](book.imap.html) тепер приймають та повертають об'єкти [IMAPConnection](class.imap-connection.html) замість ресурсів ([resource](language.types.resource.html) `imap`
    
-   The [LDAP](book.ldap.html) тепер приймають та повертають об'єкти [LDAPConnection](class.ldap-connection.html) замість ресурсів ([resource](language.types.resource.html) `ldap link`
    
-   Функції [LDAP](book.ldap.html) тепер приймають та повертають об'єкти [LDAPResult](class.ldap-result.html) замість ресурсів ([resource](language.types.resource.html) `ldap result`
    
-   Функції [LDAP](book.ldap.html) тепер приймають та повертають об'єкти [LDAPResultEntry](class.ldap-result-entry.html) замість ресурсів ([resource](language.types.resource.html) `ldap result entry`
    
-   Функції [PgSQL](book.pgsql.html) тепер приймають та повертають об'єкти [PgSqlConnection](class.pgsql-connection.html) замість ресурсів ([resource](language.types.resource.html) `pgsql link`
    
-   Функції [PgSQL](book.pgsql.html) тепер приймають та повертають об'єкти [PgSqlResult](class.pgsql-result.html) замість ресурсів ([resource](language.types.resource.html) `pgsql result`
    
-   Функції [PgSQL](book.pgsql.html) тепер приймають та повертають об'єкти [PgSqlLob](class.pgsql-lob.html) замість ресурсів ([resource](language.types.resource.html) `pgsql large object`
    
-   Функції [PSpell](book.pspell.html) тепер приймають та повертають об'єкти [PSpellDictionary](class.pspell-dictionary.html) замість ресурсів ([resource](language.types.resource.html) `pspell`
    
-   Функції [PSpell](book.pspell.html) тепер приймають та повертають об'єкти [PSpellConfig](class.pspell-config.html) замість ресурсів ([resource](language.types.resource.html) `pspell config`
    

### MySQLi

Функції [mysqlifetchfields()](mysqli-result.fetch-fields.html) і [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.html) тепер завжди повертають `0` у властивості maxlength. Це значення можна обчислити, перебираючи набір результатів та вибираючи максимальну довжину. Такий алгоритм раніше використовував PHP.

Опція **`MYSQLI_STMT_ATTR_UPDATE_MAX_LENGTH`** більше немає сенсу.

Опція **`MYSQLI_STORE_RESULT_COPY_DATA`** більше немає сенсу. Передача будь-якого значення параметр `mode` методу [mysqli::storeresult()](mysqli.store-result.html) більше немає сенсу.

[mysqli::connect()](function.mysqli-connect.html) тепер повертає **`true`** замість **`null`** у разі успішного виконання.

Режим обробки помилок за умовчанням було змінено з "silent" на "exceptions". Дивіться сторінку [Режимы обработки ошибок MySQLi](mysqli-driver.report-mode.html) для отримання додаткових відомостей про те, що це спричиняє і як явно встановити цей атрибут. Щоб відновити попередню поведінку, використовуйте: `mysqli_report(MYSQLI_REPORT_OFF);`

Класи, що розширюють [mysqlistmt::execute()](mysqli-stmt.execute.html), тепер потрібно вказати додатковий необов'язковий параметр.

### MySQLnd

INI-директива [mysqlnd.fetchdatacopy](mysqlnd.config.html#ini.mysqlnd.fetch_data_copy) було видалено. Це не повинно призводити до видимих ​​для користувача змін у поведінці.

### OpenSSL

Секретні ключі EC тепер експортуватимуться у форматі PKCS#8, а не у традиційному форматі, як і всі інші ключі.

[opensslpkcs7encrypt()](function.openssl-pkcs7-encrypt.html) і [opensslcmsencrypt()](function.openssl-cms-encrypt.html) тепер за замовчуванням використовують шифр AES-128-CBC, а чи не RC2-40. Шифр RC2-40 вважається небезпечним і не включений за промовчанням у OpenSSL 3.

### Об'єкти даних PHP

**`PDO::ATTR_STRINGIFY_FETCHES`** тепер перетворює логічні значення (bool) на `"0"` або `"1"`. Раніше логічні значення (bool) були строковими.

Виклик [PDOStatement::bindColumn()](pdostatement.bindcolumn.html) з **`PDO::PARAM_LOB`** тепер буде постійно пов'язувати результат потоку, якщо **`PDO::ATTR_STRINGIFY_FETCHES`** не увімкнуто. Раніше результатом був або потік, або рядок в залежності від драйвера бази даних і часу виконання прив'язки.

#### Драйвер MySQL

Цілі числа та числа з плаваючою комою у наборах результатів тепер повертатимуться з використанням власних типів PHP замість рядків (string) при використанні емульованих підготовлених операторів. Це відповідає поведінці своїх підготовлених операторів. Попередню поведінку можна відновити, увімкнувши опцію **`PDO::ATTR_STRINGIFY_FETCHES`**

#### Драйвер SQLite

Цілі числа та числа з плаваючою комою в наборах результатів тепер повертатимуться з використанням власних типів PHP. Попередню поведінку можна відновити, увімкнувши опцію **`PDO::ATTR_STRINGIFY_FETCHES`**

### Phar

Щоб відповідати інтерфейсу [ArrayAccess](class.arrayaccess.html) [Phar::offsetUnset()](phar.offsetunset.html) і [PharData::offsetUnset()](phardata.offsetunset.html) більше повертають логічне значення (bool).

### Стандартні функції

[versioncompare()](function.version-compare.html) більше не приймає недокументованих скорочень операторів.

Функції [htmlspecialchars()](function.htmlspecialchars.html) [htmlentities()](function.htmlentities.html) [htmlspecialcharsdecode()](function.htmlspecialchars-decode.html) [htmlentitydecode()](function.html-entity-decode.html) і [gethtmltranslationtable()](function.get-html-translation-table.html) тепер за умовчанням використовують `ENT_QUOTES | ENT_SUBSTITUTE` замість **`ENT_COMPAT`**. Це означає, що тепер `'` екранується в `&#039;`. Крім того, у разі неправильного UTF-8 замість порожнього рядка буде повернуто заміщувальний символ Unicode.

[debugzvaldump()](function.debug-zval-dump.html) тепер виводить refcount оболонок посилань з їх refcount, замість того, щоб просто додавати `&` до значення. Це більш точно моделює еталонну виставу, починаючи з PHP 7.0.

[debugzvaldump()](function.debug-zval-dump.html) тепер виводить `interned` замість фіктивного refcount для інтернованих рядків та незмінних масивів.

### Стандартна бібліотека PHP (SPL)

[SplFixedArray](class.splfixedarray.html) тепер буде закодовано в JSON як масив (array).
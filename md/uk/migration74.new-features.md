Нові можливості

-   [« Миграция с PHP 7.3.x на PHP 7.4.x](migration74.html)
    
-   [Нові класи та інтерфейси »](migration74.new-classes.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.3.x на PHP 7.4.x](migration74.html)
    
-   Нові можливості
    

## Нові можливості

### Ядро PHP

#### Типізовані властивості

Властивості класу підтримують оголошення типів.

```php
<?php
class User {
    public int $id;
    public string $name;
}
?>
```

У наведеному прикладі вище показано, що `$user->id` можна присвоїти лише значення типу int, коли як `$user->name` - Виключно значення типу string.

#### Стрілочні функції

[Стрілочні функції](functions.arrow.html) - це скорочений запис визначення функцій з неявною прив'язкою батьківської області видимості за значенням.

```php
<?php
$factor = 10;
$nums = array_map(fn($n) => $n * $factor, [1, 2, 3, 4]);
// $nums = array(10, 20, 30, 40);
?>
```

#### Обмежена коваріація типу, що повертається, і контраваріантність типу аргументу

Наступний код тепер працюватиме:

```php
<?php
class A {}
class B extends A {}

class Producer {
    public function method(): A {}
}
class ChildProducer extends Producer {
    public function method(): B {}
}
?>
```

Повна підтримка варіантності доступна лише під час використання автозавантаження. Всередині одного файлу можуть бути лише нециклічні посилання, оскільки всі класи повинні бути визначені перед тим, як на них посилатися.

#### Присвоює оператор об'єднання з null

```php
<?php
$array['key'] ??= computeDefault();
// примерно то же самое
if (!isset($array['key'])) {
    $array['key'] = computeDefault();
}
?>
```

#### Розпакування всередині масивів

```php
<?php
$parts = ['apple', 'pear'];
$fruits = ['banana', 'orange', ...$parts, 'watermelon'];
// ['banana', 'orange', 'apple', 'pear', 'watermelon'];
?>
```

#### Розділювач у числових літералах

Тепер у числових літералах між знаками можуть бути символи підкреслення.

```php
<?php
6.674_083e-11; // число с плавающей точкой
299_792_458;   // десятичное число
0xCAFE_F00D;   // шестнадцатеричное число
0b0101_1111;   // двоичное число
?>
```

#### Слабкі посилання

[Слабкі посилання](class.weakreference.html) дозволяють програмісту зберегти посилання на об'єкт, яка не завадить збирачеві сміття видалити цей об'єкт.

#### Обробка винятків із методу toString()

Викидання винятків із методу [toString()](language.oop5.magic.html#object.tostring) тепер дозволено. Раніше це призводило до фатальної помилки. Існуючі фатальні помилки, що відловлюються, при перетворенні об'єкта в рядок будуть доступні у вигляді винятків класу [Error](class.error.html)

### CURL

Крім звичайних імен файлів, клас [CURLFile](class.curlfile.html) тепер підтримує потокові обгортки, якщо модуль зібрано з версією libcurl >= 7.56.0.

### Фільтрування

Фільтр **`FILTER_VALIDATE_FLOAT`** тепер підтримує параметри `min_range` і `max_range`, з тим же змістом, що і для **`FILTER_VALIDATE_INT`**

### FFI

FFI - новий модуль, який пропонує простий спосіб виклику вбудованих функцій, доступу до вбудованих змінних, а також створювати або звертатися до структур даних у бібліотеках мовою Сі.

### ДД

Додано константу **`IMG_FILTER_SCATTER`** для застосування фільтра, що розсіюється, до зображень.

### Хешування

Доданий хеш `crc32c`використовує поліном Кастанолі. Ця реалізація алгоритму CRC32 використовується системами зберігання, такими як iSCSI, SCTP, Btrfs та ext4.

### Багатобайтові рядки

Додана функція [мбstrsplit()](function.mb-str-split.html)яка виконує те ж саме, що і [strsplit()](function.str-split.html)але працює з кодовими точками, а не з байтами.

### OPcache

Додана підтримка [предварительной загрузки кода](opcache.preloading.html)

### Регулярні вирази (сумісні з Perl)

Функції [pregreplacecallback()](function.preg-replace-callback.html) і [pregreplacecallbackarray()](function.preg-replace-callback-array.html) тепер приймають додатковий аргумент `flags` з підтримкою прапорів **`PREG_OFFSET_CAPTURE`** і **`PREG_UNMATCHED_AS_NULL`**. Він вплине на формат масиву значень, що збіглися, що передається в callback-функцію.

### PDO

Ім'я користувача та пароль тепер можна вказати як частину DSN для драйверів mysql, mssql, sybase, dblib, firebird та oci. Раніше підтримка цього була лише драйвера pgsql. Якщо ім'я користувача/пароль вказано і в конструкторі і DSN, то конструктор матиме пріоритет.

Також тепер можна екранувати знаки запитань у SQL-запитах, щоб вони не сприймалися як іменовані параметри. Використання `??` відправить один знак питання до бази даних, і, наприклад, у разі використання PostgreSQL, буде використано оператора перевірки існування ключа в JSON (`?`

### PDOOCI

Для цього драйвера тепер доступний метод [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html)

### PDOSQLite

Вираз `PDOStatement::getAttribute(PDO::SQLITE_ATTR_READONLY_STATEMENT)` дозволяє перевірити, чи доступний підготовлений запит лише читання, тобто. чи не змінює він базу даних.

`PDO::setAttribute(PDO::SQLITE_ATTR_EXTENDED_RESULT_CODES, true)` дозволяє використовувати розширені коди результату SQLite3 [PDOStatement::errorInfo()](pdostatement.errorinfo.html)

### SQLite3

Доданий метод **SQLite3::lastExtendedErrorCode()** для отримання останнього розширеного коду результату.

Доданий метод `SQLite3::enableExtendedResultCodes($enable = true)`, який змусить метод [SQLite3::lastErrorCode()](sqlite3.lasterrorcode.html) повертати розширені коди результатів.

### Стандартне

#### striptags() з масивом імен тегів

Функція [striptags()](function.strip-tags.html) тепер також приймає масив дозволених тегів: замість `strip_tags($str, '<a><p>')` тепер можна написати `strip_tags($str, ['a', 'p'])`

#### Користувальницька серіалізація об'єктів

Додано новий механізм серіалізації об'єктів, що використовує два нових магічних методи: `__serialize` і `__unserialize`

```php
<?php
// Возвращает массив, содержащий все необходимое состояние объекта.
public function __serialize(): array;

// Восстанавливает состояние объекта из указанного массива данных.
public function __unserialize(array $data): void;
?>
```

Новий механізм серіалізації замінює інтерфейс [Serializable](class.serializable.html), який у майбутньому буде оголошено застарілим.

#### Функції злиття масивів без аргументів

Функції [arraymerge()](function.array-merge.html) і [arraymergerecursive()](function.array-merge-recursive.html) тепер можуть викликатися без жодних аргументів, і тоді вони повернуть порожній масив. Це корисно у поєднанні з оператором розширення, наприклад, `array_merge(...$arrays)`

#### Функція [procopen()](function.proc-open.html)

[procopen()](function.proc-open.html) тепер приймає масив замість рядка для виконання команди. У цьому випадку процес буде відкритий безпосередньо (без командної оболонки), а PHP екранує будь-який аргумент.

```php
<?php
proc_open(['php', '-r', 'echo "Привет, мир\n";'], $descriptors, $pipes);
?>
```

Функція [procopen()](function.proc-open.html) тепер підтримує дескриптори `redirect` і `null`

```php
<?php
// То же самое, что и 2>&1 в командной оболочке
proc_open($cmd, [1 => ['pipe', 'w'], 2 => ['redirect', 1]], $pipes);
// То же самое, что и 2>/dev/null или 2>nul в командной оболочке
proc_open($cmd, [1 => ['pipe', 'w'], 2 => ['null']], $pipes);
?>
```

#### argon2i(d) без libargon

Функція [passwordhash()](function.password-hash.html) тепер підтримує варіанти хешування argon2i та argon2id з модуля sodium, коли PHP зібраний без libargon.
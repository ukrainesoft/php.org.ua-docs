---
navigation:
  - migration72.md: « Миграция с PHP 7.1.x на PHP 7.2.x
  - migration72.new-functions.html: Нові функції »
  - index.md: PHP Manual
  - migration72.md: Миграция с PHP 7.1.x на PHP 7.2.x
title: Нові можливості
---
## Нові можливості

### Новий тип object

Було введено новий тип, object, який може використовуватися в параметрах, що передаються (контраваріантність) і повертаються значеннях (коваріантність) для будь-яких об'єктів.

```php
<?php

function test(object $obj) : object
{
    return new SplQueue();
}

test(new StdClass());
```

### Завантаження модуля на ім'я

Для підвантажуваних модулів більше не потрібно вказувати розширення файлу (`.so` для Unix або `.dll` для Windows). Це допускається у файлі php.ini, а також функції [dl()](function.dl.md)

### Дозволено перевизначення абстрактних методів

Абстрактні методи тепер можна перевизначити, якщо абстрактний клас успадковується від іншого абстрактного класу.

```php
<?php

abstract class A
{
    abstract function test(string $s);
}
abstract class B extends A
{
    // переопределён - всё ещё сохраняя контравариантность для параметров и ковариантность для возвращаемых значений
    abstract function test($s) : int;
}
```

### [Sodium](book.sodium.md) тепер є основним модулем

Сучасна криптографічна бібліотека Sodium тепер стала основним модулем PHP (як модуль sodium).

Дивіться розділ [Sodium](book.sodium.md) для отримання повної інформації.

### Додано хешування пароля за допомогою Argon2

Було додано алгоритм Argon2 в [API хеширования пароля](book.password.md), де доступні такі константи:

-   **`PASSWORD_ARGON2I`**
-   **`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**
-   **`PASSWORD_ARGON2_DEFAULT_TIME_COST`**
-   **`PASSWORD_ARGON2_DEFAULT_THREADS`**

### Розширені типи рядків для [PDO](book.pdo.md)

Тип рядка PDO був розширений для підтримки національних наборів символів при емуляції запитів, що готуються. Додані нові константи:

-   **`PDO::PARAM_STR_NATL`**
-   **`PDO::PARAM_STR_CHAR`**
-   **`PDO::ATTR_DEFAULT_STR_PARAM`**

Ці константи використовують у побітовому `OR` з константою **`PDO::PARAM_STR`**

```php
<?php

$db->quote('über', PDO::PARAM_STR | PDO::PARAM_STR_NATL);
```

### Додаткова налагоджувальна інформація при емуляції запитів, що готуються [PDO](book.pdo.md)

Метод [PDOStatement::debugDumpParams()](pdostatement.debugdumpparams.md) було оновлено, щоб увімкнути SQL до відправки в БД, де буде показаний повний необроблений запит (включаючи замінені параметри зі своїми пов'язаними значеннями). Це було додано для допомоги у налагодженні емуляції запитів, що готуються (і тому це буде доступно тільки при включеній емуляції підготовлюваних запитів).

### Підтримка розширених операцій на [LDAP](book.ldap.md)

Було додано підтримку EXOP модуль LDAP. Стали доступні такі функції та константи:

-   [ldapparseexop()](function.ldap-parse-exop.md)
-   [ldapexop()](function.ldap-exop.md)
-   [ldapexoppasswd()](function.ldap-exop-passwd.md)
-   [ldapexopwhoami()](function.ldap-exop-whoami.md)
-   **`LDAP_EXOP_START_TLS`**
-   **`LDAP_EXOP_MODIFY_PASSWD`**
-   **`LDAP_EXOP_REFRESH`**
-   **`LDAP_EXOP_WHO_AM_I`**
-   **`LDAP_EXOP_TURN`**

### Інформація про адресу в модулі [сокетів](book.sockets.md)

Модуль сокетів має можливість шукати адресну інформацію, а також підключатися до неї, зв'язуватися з нею і пояснювати її. Для цього були додані такі чотири функції:

-   [socketaddrinfolookup()](function.socket-addrinfo-lookup.md)
-   [socketaddrinfoconnect()](function.socket-addrinfo-connect.md)
-   [socketaddrinfobind()](function.socket-addrinfo-bind.md)
-   [socketaddrinfoexplain()](function.socket-addrinfo-explain.md)

### Розширення типу параметра

Типи параметрів із перевизначених методів та реалізацій інтерфейсів тепер можуть бути опущені. Це все ще відповідає LSP, оскільки параметри типів є контраваріантними.

```php
<?php

interface A
{
    public function Test(array $input);
}

class B implements A
{
    public function Test($input){} // тип параметра не указан $input
}
```

### Дозволена завершальна кома для згрупованих просторів імен

Завершальна кома тепер може бути додана до синтаксису угруповання use, що з'явився в PHP 7.0.

```php
<?php

use Foo\Bar\{
    Foo,
    Bar,
    Baz,
};
```

### Підтримка [procnice()](function.proc-nice.md) для Windows

Функція [procnice()](function.proc-nice.md) тепер підтримується у Windows.

### Підтримка порядку байт у [pack()](function.pack.md) і [unpack()](function.unpack.md)

Функції [pack()](function.pack.md) і [unpack()](function.unpack.md) тепер підтримують типи float та double як у прямому, так і у зворотному порядку байт.

### Поліпшення в модулі [EXIF](book.exif.md)

Модуль EXIF ​​оновлено для підтримки більшої кількості форматів. Це означає, що специфічні теги правильно обробляються при розборі зображень функцією [exifreaddata()](function.exif-read-data.md). Нові формати, що підтримуються:

-   Samsung
-   DJI
-   Panasonic
-   Sony
-   Pentax
-   Minolta
-   Sigma/Foveon
-   AGFA
-   Kyocera
-   Ricoh
-   Epson

Функції [exifreaddata()](function.exif-read-data.html) і [exifthumbnail()](function.exif-thumbnail.md) тепер приймають потоки як свої перші аргументи.

### Нова функціональність у [PCRE](book.pcre.md)

-   Доданий модифікатор `J` для встановлення PCREDUPNAMES.

### [SQLite3](book.sqlite3.md) дозволяє записувати BLOB

Тепер [SQLite3::openBlob()](sqlite3.openblob.md) вміє відкривати поля типу BLOB для запису. Раніше для таких полів було доступне лише читання.

### Зворотні дзвінки [Oracle OCI8](book.oci8.md) Transparent Application Failover

Додана підтримка [зворотних викликів Oracle Database Transparent Application Failover (TAF)](oci8.taf.md). TAF дозволяє програмам PHP OCI8 автоматично перепідключатися до попередньо налаштованої бази даних при порушенні з'єднання. Нова підтримка зворотного дзвінка TAF дозволяє програмам відстежувати та контролювати перепідключення під час відновлення.

### Поліпшення в модулі [ZIP](book.zip.md)

Додано підтримку читання та запису зашифрованих архівів (потрібно libzip 1.2.0).

Клас [ZipArchive](class.ziparchive.md) тепер реалізує інтерфейс [Countable](class.countable.md)

Потік `zip://` тепер приймає контекстну опцію `'password'`

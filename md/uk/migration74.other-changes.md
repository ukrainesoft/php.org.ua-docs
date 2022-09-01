---
navigation:
  - migration74.removed-extensions.html: « Видалені модулі
  - migration74.windows-support.html: Поддержка Windows »
  - index.md: PHP Manual
  - migration74.md: Миграция с PHP 7.3.x на PHP 7.4.x
title: Інші зміни
---
## Інші зміни

### Поліпшення продуктивності

#### Ядро PHP

Додано спеціальний опкод віртуальної машини для функції [arraykeyexists()](function.array-key-exists.html), що покращує продуктивність цієї функції, якщо значення параметра може бути статично дозволено. У коді, який використовує простір імен, можливо буде потрібно використання абсолютного імені (`\array_key_exists()`) або ж явний імпорт функції.

#### Регулярні вирази (сумісні з Perl)

Коли функція [pregmatch()](function.preg-match.html) у режимі UTF-8 (модифікатор `"u"`) неодноразово викликається для одного і того ж рядка (можливо, на різних позиціях), перевірка правильності UTF-8 буде виконана лише один раз.

### Зміни обробки INI-файлів

[zend.exceptionignoreargs](ini.core.html#ini.zend.exception-ignore-args) - нова INI-директива для включення або виключення аргументів з трасування стека, отриманих у винятках.

[opcache.preloaduser](opcache.configuration.html#ini.opcache.preload-user) - нова INI-директива для встановлення користувача, з-під якого має виконуватися код попереднього завантаження, інакше це буде root (не допускається з міркувань безпеки).

### Міграція на pkg-config

Багато модулів тепер використовують виключно pkg-config, щоб визначати залежності бібліотек. Як правило, це означає, що замість **\-with-foo-dir=DIR** використовується тільки **\-with-foo**. Користувацькі шляхи до бібліотек можуть бути вказані або шляхом додавання додаткових каталогів у `PKG_CONFIG_PATH`, або шляхом явного вказівки параметрів компіляції через `FOO_CFLAGS` і `FOO_LIBS`

Наступні модулі та SAPI були порушені цією зміною:

-   CURL:
    -   Опція **\-with-curl** більше не приймає каталог.
-   Enchant:
    -   Опція **\-with-enchant** більше не приймає каталог.
-   FPM:
    -   Опція **\-with-fpm-systemd** тепер використовує тільки pkg-config для перевірки libsystem. Мінімальна обов'язкова версія libsystemd – 209.
-   GD:
    -   Опція **\-with-gd** перейменована в **\-enable-gd** (має бути включений модуль чи ні), а опція **\-with-external-gd** використовує зовнішню бібліотеку libgd замість тієї, яка йде в комплекті.
    -   Опція **\-with-png-dir** видалено. Наявність libpng тепер є обов'язковою.
    -   Опція **\-with-zlib-dir** видалено. Наявність zlib тепер є обов'язковою.
    -   Опція **\-with-freetype-dir** перейменована в **\-with-freetype**
    -   Опція **\-with-jpeg-dir** перейменована в **\-with-jpeg**
    -   Опція **\-with-webp-dir** перейменована в **\-with-webp**
    -   Опція **\-with-xpm-dir** перейменована в **\-with-xpm**
-   IMAP:
    -   Опція **\-with-kerberos-systemd** більше не приймає каталог.
-   Intl:
    -   Опція **\-with-icu-dir** видалено. Якщо передано **\-enable-intl**тоді завжди потрібна наявність libicu.
-   LDAP:
    -   Опція **\-with-ldap-sasl** більше не приймає каталог.
-   Libxml:
    -   Опція **\-with-libxml-dir** видалено.
    -   Опція **\-enable-libxml** перейменована в **\-with-libxml**
    -   Опція **\-with-libexpat-dir** перейменована в **\-with-expat** та більше не приймає каталог.
-   Litespeed:
    -   Опція **\-with-litespeed** перейменована в **\-enable-litespeed**
-   Mbstring:
    -   Опція **\-with-onig** видалено. Якщо **\-disable-mbregex** не вказано, потрібно libonig.
-   ODBC:
    -   Опція **\-with-iodbc** більше не приймає каталог.
    -   Опція **\-with-unixODBC** без каталогу тепер використовує pkg-config (переважно). Каталог, як і раніше, можна вказати для старих версій без libodbc.pc.
-   OpenSSL:
    -   Опція **\-with-openssl** більше не приймає каталог.
-   PCRE:
    -   Опція **\-with-pcre-regex** видалено. Замість цього **\-with-external-pcre** дозволяє використовувати зовнішню PCRE-бібліотеку замість вбудованої.
-   PDOSQLite:
    -   Опція **\-with-pdo-sqlite** більше не приймає каталог.
-   Readline:
    -   Опція **\-with-libedit** більше не приймає каталог.
-   Sodium:
    -   Опція **\-with-sodium** більше не приймає каталог.
-   SQLite3:
    -   Опція **\-with-sqlite3** більше не приймає каталог.
-   XSL:
    -   Опція **\-with-xsl** більше не приймає каталог.
-   Zip:
    -   Опція **\-with-libzip** видалено.
    -   Опція **\-enable-zip** перейменована в **\-with-zip**

### Екранування CSV

[fputcsv()](function.fputcsv.md) [fgetcsv()](function.fgetcsv.md) [SplFileObject::fputcsv()](splfileobject.fputcsv.md) [SplFileObject::fgetcsv()](splfileobject.fgetcsv.md) і [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md) тепер приймаємо порожній рядок у аргументі `$escape`. Це відключить пропрієтарний механізм екранування PHP.

Поведінка функції [strgetcsv()](function.str-getcsv.html) було відповідним чином скориговано (раніше порожній рядок був ідентичний використанню значення за умовчанням).

Метод [SplFileObject::getCsvControl()](splfileobject.getcsvcontrol.md) тепер може повертати порожній рядок для третього елемента масиву, відповідно.

### Фільтрування даних

Модуль [filter](book.filter.md) більше не підтримує **\--with-pcre-dir** для Unix-складання і тому може бути спокійно зібраний для загального користування за допомогою **./configure**

### ДД

Поведінка функції [imagecropauto()](function.imagecropauto.md) у вбудованій бібліотеці libgd було синхронізовано із системною бібліотекою libgd:

-   **`IMG_CROP_DEFAULT`** у разі невдалого виконання не замінюється на **`IMG_CROP_SIDES`**
-   Порогове значення кадрування тепер розраховується з алгоритму системної бібліотеки libgd

Значення за замовчуванням `$mode` [imagecropauto()](function.imagecropauto.md) було змінено на **`IMG_CROP_DEFAULT`**; передача `-1` тепер оголошено застарілою.

[imagescale()](function.imagescale.md) тепер підтримує масштабування зі збереженням співвідношення сторін до фіксованої висоти під час передачі `-1` у параметр `$new_width`

### Фреймворк хеш-кодів HASH

Модуль [hash](book.hash.md) більше не можна відключити, тепер він є невід'ємною частиною будь-якої PHP-складання, подібно до модуля [date](book.datetime.md)

### Intl

Модуль [intl](book.intl.md) тепер вимагає щонайменше ICU 50.1.

Клас [ResourceBundle](class.resourcebundle.md) тепер реалізує [Countable](class.countable.md)

### Полегшений протокол доступу до каталогів (LDAP)

Підтримка nsldap та umichldap було видалено.

### Libxml

Усі модулі на основі libxml тепер вимагають libxml версії 2.7.6 або новіші.

### Багатобайтові рядки

Бібліотека oniguruma більше не йде в комплекті з PHP, замість неї в системі має бути libonig. Як альтернативу можна вказати **\--disable-mbregex**, щоб вимкнути компонент mbregex.

### OPcache

Конфігураційні опції **\-disable-opcache-file** і **\-enable-opcache-file** видалені на користь використання INI-директиви [opcache.filecache](opcache.configuration.html#ini.opcache.file-cache)

### Хешування паролів

Функції [passwordhash()](function.password-hash.html) і [passwordneedsrehash()](function.password-needs-rehash.html) тепер приймають рядок, що обнулюється, (string) і ціле число (int) в аргументі `$algo`

### PEAR

Установка PEAR (разом із PECL) більше не ввімкнена за замовчуванням. Її можна явно увімкнути, використовуючи **\-with-pear**. Ця опція оголошена застарілою та може бути видалена в майбутньому.

### Reflection

Змінено числові значення констант-модифікаторів (`IS_ABSTRACT` `IS_DEPRECATED` `IS_EXPLICIT_ABSTRACT` `IS_FINAL` `IS_IMPLICIT_ABSTRACT` `IS_PRIVATE` `IS_PROTECTED` `IS_PUBLIC` і `IS_STATIC`) у класах [ReflectionClass](class.reflectionclass.md) [ReflectionFunction](class.reflectionfunction.md) [ReflectionMethod](class.reflectionmethod.md) [ReflectionObject](class.reflectionobject.md) і [ReflectionProperty](class.reflectionproperty.md)

### SimpleXML

Клас [SimpleXMLElement](class.simplexmlelement.md) тепер реалізує [Countable](class.countable.md)

### SQLite3

Вбудована бібліотека libsqlite у збірці видалена. Для складання модуля [SQLite3](book.sqlite3.md) тепер потрібно libsqlite3 ≥ 3.7.4. Щоб зібрати модуль [PDOSQLite](ref.pdo-sqlite.html) обов'язково потрібний libsqlite3 ≥ 3.5.0.

Серіалізація та десеріалізація [SQLite3](class.sqlite3.md) [SQLite3Stmt](class.sqlite3stmt.md) і [SQLite3Result](class.sqlite3result.md) тепер явно заборонено. Раніше серіалізація екземплярів цих класів була можливою, але десеріалізація робила об'єкти невикористовуваними для подальшої роботи.

Нотацію `@param` тепер можна також використовувати для позначення параметрів SQL-запиту.

### Zip

Вбудована бібліотека libzip видалена. Тепер обов'язково наявність у системі бібліотеки libzip >= 0.11, щоб зібрати модуль [zip](book.zip.md)

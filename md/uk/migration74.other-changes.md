Інші зміни

-   [« Удалённые модули](migration74.removed-extensions.html)
    
-   [Поддержка Windows »](migration74.windows-support.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.3.x на PHP 7.4.x](migration74.html)
    
-   Інші зміни
    

## Інші зміни

### Поліпшення продуктивності

#### Ядро PHP

Додано спеціальний опкод віртуальної машини для функції [array\_key\_exists()](function.array-key-exists.html), що покращує продуктивність цієї функції, якщо значення параметра може бути статично дозволено. У коді, який використовує простір імен, можливо буде потрібно використання абсолютного імені (`\array_key_exists()`) або ж явний імпорт функції.

#### Регулярні вирази (сумісні з Perl)

Коли функція [preg\_match()](function.preg-match.html) у режимі UTF-8 (модифікатор `"u"`) неодноразово викликається для одного і того ж рядка (можливо, на різних позиціях), перевірка правильності UTF-8 буде виконана лише один раз.

### Зміни обробки INI-файлів

[zend.exception\_ignore\_args](ini.core.html#ini.zend.exception-ignore-args) - нова INI-директива для включення або виключення аргументів з трасування стека, отриманих у винятках.

[opcache.preload\_user](opcache.configuration.html#ini.opcache.preload-user) - нова INI-директива для встановлення користувача, з-під якого має виконуватися код попереднього завантаження, інакше це буде root (не допускається з міркувань безпеки).

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

[fputcsv()](function.fputcsv.html) [fgetcsv()](function.fgetcsv.html) [SplFileObject::fputcsv()](splfileobject.fputcsv.html) [SplFileObject::fgetcsv()](splfileobject.fgetcsv.html) і [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.html) тепер приймаємо порожній рядок у аргументі `$escape`. Це відключить пропрієтарний механізм екранування PHP.

Поведінка функції [str\_getcsv()](function.str-getcsv.html) було відповідним чином скориговано (раніше порожній рядок був ідентичний використанню значення за умовчанням).

Метод [SplFileObject::getCsvControl()](splfileobject.getcsvcontrol.html) тепер може повертати порожній рядок для третього елемента масиву, відповідно.

### Фільтрування даних

Модуль [filter](book.filter.html) більше не підтримує **\--with-pcre-dir** для Unix-складання і тому може бути спокійно зібраний для загального користування за допомогою **./configure**

### ДД

Поведінка функції [imagecropauto()](function.imagecropauto.html) у вбудованій бібліотеці libgd було синхронізовано із системною бібліотекою libgd:

-   **`IMG_CROP_DEFAULT`** у разі невдалого виконання не замінюється на **`IMG_CROP_SIDES`**
-   Порогове значення кадрування тепер розраховується з алгоритму системної бібліотеки libgd

Значення за замовчуванням `$mode` [imagecropauto()](function.imagecropauto.html) було змінено на **`IMG_CROP_DEFAULT`**; передача `-1` тепер оголошено застарілою.

[imagescale()](function.imagescale.html) тепер підтримує масштабування зі збереженням співвідношення сторін до фіксованої висоти під час передачі `-1` у параметр `$new_width`

### Фреймворк хеш-кодів HASH

Модуль [hash](book.hash.html) більше не можна відключити, тепер він є невід'ємною частиною будь-якої PHP-складання, подібно до модуля [date](book.datetime.html)

### Intl

Модуль [intl](book.intl.html) тепер вимагає щонайменше ICU 50.1.

Клас [ResourceBundle](class.resourcebundle.html) тепер реалізує [Countable](class.countable.html)

### Полегшений протокол доступу до каталогів (LDAP)

Підтримка nsldap та umichldap було видалено.

### Libxml

Усі модулі на основі libxml тепер вимагають libxml версії 2.7.6 або новіші.

### Багатобайтові рядки

Бібліотека oniguruma більше не йде в комплекті з PHP, замість неї в системі має бути libonig. Як альтернативу можна вказати **\--disable-mbregex**, щоб вимкнути компонент mbregex.

### OPcache

Конфігураційні опції **\-disable-opcache-file** і **\-enable-opcache-file** видалені на користь використання INI-директиви [opcache.file\_cache](opcache.configuration.html#ini.opcache.file-cache)

### Хешування паролів

Функції [password\_hash()](function.password-hash.html) і [password\_needs\_rehash()](function.password-needs-rehash.html) тепер приймають рядок, що обнулюється, (string) і ціле число (int) в аргументі `$algo`

### PEAR

Установка PEAR (разом із PECL) більше не ввімкнена за замовчуванням. Її можна явно увімкнути, використовуючи **\-with-pear**. Ця опція оголошена застарілою та може бути видалена в майбутньому.

### Reflection

Змінено числові значення констант-модифікаторів (`IS_ABSTRACT` `IS_DEPRECATED` `IS_EXPLICIT_ABSTRACT` `IS_FINAL` `IS_IMPLICIT_ABSTRACT` `IS_PRIVATE` `IS_PROTECTED` `IS_PUBLIC` і `IS_STATIC`) у класах [ReflectionClass](class.reflectionclass.html) [ReflectionFunction](class.reflectionfunction.html) [ReflectionMethod](class.reflectionmethod.html) [ReflectionObject](class.reflectionobject.html) і [ReflectionProperty](class.reflectionproperty.html)

### SimpleXML

Клас [SimpleXMLElement](class.simplexmlelement.html) тепер реалізує [Countable](class.countable.html)

### SQLite3

Вбудована бібліотека libsqlite у збірці видалена. Для складання модуля [SQLite3](book.sqlite3.html) тепер потрібно libsqlite3 ≥ 3.7.4. Щоб зібрати модуль [PDO\_SQLite](ref.pdo-sqlite.html) обов'язково потрібний libsqlite3 ≥ 3.5.0.

Серіалізація та десеріалізація [SQLite3](class.sqlite3.html) [SQLite3Stmt](class.sqlite3stmt.html) і [SQLite3Result](class.sqlite3result.html) тепер явно заборонено. Раніше серіалізація екземплярів цих класів була можливою, але десеріалізація робила об'єкти невикористовуваними для подальшої роботи.

Нотацію `@param` тепер можна також використовувати для позначення параметрів SQL-запиту.

### Zip

Вбудована бібліотека libzip видалена. Тепер обов'язково наявність у системі бібліотеки libzip >= 0.11, щоб зібрати модуль [zip](book.zip.html)
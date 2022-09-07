---
navigation:
  - migration74.constants.md: « Нові глобальні константи
  - migration74.deprecated.md: Устаревшая функциональность »
  - index.md: PHP Manual
  - migration74.md: Миграция с PHP 7.3.x на PHP 7.4.x
title: 'Зміни, що ламають зворотну сумісність'
---
## Зміни, що ламають зворотну сумісність

### Ядро PHP

#### Масивоподібне звернення до не масивів

Спроба використовувати значення типу null, bool, int, float або resource як масив (наприклад, `$null["key"]`) Тепер створить повідомлення.

#### Функція [getdeclaredclasses()](function.get-declared-classes.md)

Функція [getdeclaredclasses()](function.get-declared-classes.md) більше не повертає анонімних класів, які ще не були створені.

#### Ключове слово `fn`

`fn` тепер зарезервоване ключове слово. Зокрема, воно більше не може використовуватися як ім'я функції або класу. Але при цьому цим ключовим словом можна назвати ім'я методу або константи в класі.

#### Тег `<?php` наприкінці файлу

Використання `<?php` в кінці файлу (без завершального нового рядка) тепер інтерпретуватиметься як PHP-тег. Раніше він оброблявся або як короткий тег з наступним літералом `php` і приводив до синтаксичної помилки (при `short_open_tag=1`), або сприймався як рядковий літерал `<?php` (в разі `short_open_tag=0`

#### Поточні обгортки

При використанні include/require з потоком, [streamWrapper::streamsetoption()](streamwrapper.stream-set-option.md) буде викликатись з параметром **`STREAM_OPTION_READ_BUFFER`**. Для користувальницьких потокових обгорток, можливо, знадобиться реалізація методу [streamWrapper::streamsetoption()](streamwrapper.stream-set-option.md), щоб прибрати попередження (як правило, вистачає тільки повернення **`false`**

#### Серіалізація

Видалено формат серіалізації `o`. Оскільки він ніколи не використовується самим PHP, він тільки міг порушити десеріалізацію рядків, створених вручну.

#### Константи алгоритму пароля

Ідентифікатори алгоритму хешування паролів тепер рядки, що обнулюються, а не цілі числа.

-   **`PASSWORD_DEFAULT`** раніше було цілочисленним 1; тепер рядок '2y' (у PHP 7.4.0, 7.4.1 та 7.4.2 було **`null`**
-   **`PASSWORD_BCRYPT`** раніше було цілочисленним 1; тепер рядок '2y'
-   **`PASSWORD_ARGON2I`** раніше було цілочисленним 2; тепер рядок 'argon2i'
-   **`PASSWORD_ARGON2ID`** раніше було цілочисленним 3; тепер рядок 'argon2id'

Програми, які правильно використовують константи PASSWORDDEFAULT, PASSWORDBCRYPT, PASSWORDARGON2I та PASSWORDARGON2ID, працюватимуть як і раніше.

#### Функція [htmlentities()](function.htmlentities.md)

Функція [htmlentities()](function.htmlentities.md) тепер буде видавати повідомлення (замість попередження рівня ESTRICT), якщо воно використовується з кодуванням, для якого підтримується лише перетворення основних символів. У цьому випадку вона еквівалентна використанню [htmlspecialchars()](function.htmlspecialchars.md)

#### Функції [fread()](function.fread.md) і [fwrite()](function.fwrite.md)

Функції [fread()](function.fread.md) і [fwrite()](function.fwrite.md) тепер повертатимуть \*\*`false`\*\*якщо операція не вдалася. Раніше повертався порожній рядок або 0. До помилок EAGAIN/EWOULDBLOCK це не стосується.

Ці функції тепер також викликають повідомлення при невдалому виконанні, наприклад, під час запису файловий ресурс, призначений лише читання.

### Обчислення над числами з довільною точністю BCMath

Тепер функції BCMath видаватимуть попередження, якщо передано число з помилкою, наприклад, `"32foo"`. Подібний аргумент, як і раніше, буде інтерпретовано як нуль.

### CURL

Спроба серіалізації класу [CURLFile](class.curlfile.md) тепер створить виняток. Раніше виняток викидався лише за десеріалізації.

Використання **`CURLPIPE_HTTP1`** оголошено застарілим і не підтримуватиметься з версії cURL 7.62.0.

Параметр `$version` функції [curlversion()](function.curl-version.md) оголошено застарілим. Якщо передається значення, не рівне **`CURLVERSION_NOW`** за промовчанням буде викликано попередження, а параметр проігноровано.

### дата і час

Виклик [vardump()](function.var-dump.md) або схожої налагоджувальної функції з екземпляром [DateTime](class.datetime.md) або [DateTimeImmutable](class.datetimeimmutable.md) більше не залишає після виконання доступних властивостей.

Порівняння об'єктів [DateInterval](class.dateinterval.md) (з використанням `==` `<` і т.д.) тепер створює попередження і завжди повертає **`false`**. Раніше всі об'єкти [DateInterval](class.dateinterval.md) вважалися однаковими, якщо вони не мали властивостей.

### Intl

Значення параметрів за замовчуванням у функціях [idnтоascii()](function.idn-to-ascii.md) і [idnтоutf8()](function.idn-to-utf8.md) тепер **`INTL_IDNA_VARIANT_UTS46`** замість застарілого **`INTL_IDNA_VARIANT_2003`**

### MySQLi

Функціональність вбудованого сервера видалено. Вона була зламана як мінімум із PHP 7.0.

Недокументована властивість `mysqli::$stat` було видалено на користь використання [mysqli::stat()](mysqli.stat.md)

### OpenSSL

Функція [opensslrandompseudobytes()](function.openssl-random-pseudo-bytes.md) тепер викидатиме виняток у ситуаціях, що й функція [randombytes()](function.random-bytes.md). Зокрема, викидається [Error](class.error.md), якщо кількість запрошених байтів менша або дорівнює нулю. Виняток [Exception](class.exception.md) викидається, якщо не отримано достатньої випадковості. Аргумент `$crypto_strong` гарантовано завжди дорівнюватиме \*\*`true`\*\*якщо функція нічого не викидає, тому явно перевіряти його не потрібно.

### Регулярні вирази (сумісні Perl)

При використанні прапора **`PREG_UNMATCHED_AS_NULL`**, що завершують несхожі підмаски тепер будуть мати значення **`null`** (або `[null, -1]`, якщо увімкнено збереження позиції підмаски). Це означає, що розмір `$matches` завжди буде однаковим.

### Об'єкти даних PHP (PDO)

Спроба серіалізувати екземпляр [PDO](class.pdo.md) або [PDOStatement](class.pdostatement.md) тепер створить [Exception](class.exception.md), а не [PDOException](class.pdoexception.md)за аналогією з іншими внутрішніми класами, які не підтримують серіалізацію.

### Reflection

Об'єкти Reflection тепер створюють виняток, якщо спробувати серіалізувати їх. Серіалізація об'єктів Reflection ніколи не підтримувалась і призводила до пошкодження об'єктів Reflection. Наразі це було явно заборонено.

Змінилися значення констант класів [ReflectionClassConstant](class.reflectionclassconstant.md) [ReflectionMethod](class.reflectionmethod.md) і [ReflectionProperty](class.reflectionproperty.md)

### Стандартна бібліотека PHP (SPL)

Виклик [getobjectvars()](function.get-object-vars.md) з екземпляром [ArrayObject](class.arrayobject.md) тепер завжди повертатиме властивості самого [ArrayObject](class.arrayobject.md) (або підкласу). Раніше він повертав значення упакованого масиву/об'єкта, якщо не було вказано прапор **`ArrayObject::STD_PROP_LIST`**

Інші порушені операції:

-   **ReflectionObject::getProperties()**
-   [reset()](function.reset.md) [current()](function.current.md) і т.д. Використовуйте натомість методи [Iterator](class.iterator.md)
-   Ймовірно, решта працює з властивостями об'єкта при доступі у вигляді списку, наприклад, [arraywalk()](function.array-walk.md)

На приведення типу `(array)` ці зміни не вплинуть. Вони, як і раніше, повертають або упакований масив, або властивості. [ArrayObject](class.arrayobject.md), залежно від того, чи використовується прапор **`ArrayObject::STD_PROP_LIST`**

Метод [SplPriorityQueue::setExtractFlags()](splpriorityqueue.setextractflags.md) викине виняток, якщо передано нуль. Раніше це призводило до фатальної помилки, що відловлюється, при наступній операції вилучення.

[ArrayObject](class.arrayobject.md) [ArrayIterator](class.arrayiterator.md) [SplDoublyLinkedList](class.spldoublylinkedlist.md) і [SplObjectStorage](class.splobjectstorage.md) тепер підтримують `__serialize()` і `__unserialize()` на додаток до інтерфейсу [Serializable](class.serializable.md). Тому тепер створені в більш старих версіях PHP серіалізовані дані все ще можуть бути неправильно оброблені. Однак нові створені серіалізовані дані в PHP 7.4 не сприйматимуться в більш старих версіях.

### Лексер (Tokenizer)

Функція [tokengetall()](function.token-get-all.md) тепер відобразить мітку **`T_BAD_CHARACTER`** у разі виявлення непередбачених символів у потоці міток.

### Вхідні Cookies

Починаючи з PHP 7.4.11 *імена* вхідні cookie більше не декодуються з URL-закодованого рядка з міркувань безпеки.

---
navigation:
  - migration80.md: « Міграція з PHP 7.4.x на PHP 8.0.x
  - migration80.incompatible.md: 'Зміни, що ламають зворотну сумісність »'
  - index.md: PHP Manual
  - migration80.md: Міграція з PHP 7.4.x на PHP 8.0.x
title: Нова функціональність
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Нова функціональність

### Ядро PHP

#### Іменовані аргументи

Добавлена поддержка[іменованих аргументів](functions.arguments.md#functions.named-arguments)

#### Атрибути

Добавлена поддержка[атрибутів](language.attributes.md)

#### Оголошення властивостей у конструкторі

Добавлена поддержка[визначення властивостей у конструкторі](language.oop5.decon.md#language.oop5.decon.constructor.promotion) (Оголошення властивостей у сигнатурі конструктора).

#### Об'єднання типів

Добавлена поддержка[об'єднання типів](language.types.declarations.md#language.types.declarations.composite.union)

#### Вираз Match

Добавлена поддержка[вирази `match`](control-structures.match.md)

#### Оператор Nullsafe

Добавлена поддержка[оператора Nullsafe](language.oop5.basic.md#language.oop5.basic.nullsafe) `?->`

#### Інші нові функції

-   Добавлен класс[WeakMap](class.weakmap.md)
    
-   Добавлен класс[ValueError](class.valueerror.md)
    
-   Будь-яка кількість параметрів функції тепер може бути замінена варіативним аргументом за сумісності типів. Наприклад, тепер наступний код є допустимим:
    
    ```php
    <?php
    class A {
         public function method(int $many, string $parameters, $here) {}
    }
    class B extends A {
         public function method(...$everything) {}
    }
    ?>
    ```
    
-   static (як у "пізнім статичному зв'язуванні") тепер можна використовувати як тип, що повертається:
    
    ```php
    <?php
    class Test {
         public function create(): static {
              return new static();
         }
    }
    ?>
    ```
    
-   Тепер можна отримати ім'я класу об'єкта за допомогою`$object::class`. Результат такий самий, що й`get_class($object)`
    
-   [`new`](language.oop5.basic.md#language.oop5.basic.new) і [`instanceof`](language.operators.type.md)тепер можна використовувати з довільними виразами, використовуючи`new (expression)(...$args)`и`$obj instanceof (expression)`
    
-   Було внесено деякі виправлення узгодженості до синтаксису змінних, наприклад, тепер дозволено запис`Foo::BAR::$baz`
    
-   Доданий інтерфейс[Stringable](class.stringable.md), який автоматично реалізується, якщо в класі визначено метод[\_\_toString()](language.oop5.magic.md#object.tostring)
    
-   Тепер трейти можуть визначити абстрактні закриті методи. Такі методи мають бути реалізовані класом за допомогою трейту.
    
-   `throw`тепер можна використовувати як вираз. Це означає, що тепер можливе таке:
    
    ```php
    <?php
    $fn = fn() => throw new Exception('Виключення у стрілочній функції');
    $user = $session->user ?? throw new Exception('Має бути користувач');
    ```
    
-   У списках параметрів тепер дозволена необов'язкова завершальна кома.
    
    ```php
    <?php
    function functionWithLongSignature(
        Type1 $parameter1,
        Type2 $parameter2, // <-- Ця кома тепер дозволена.
    ) {
    }
    ```
    
-   Тепер можна написати`catch (Exception)`для перехоплення виключення, не зберігаючи їх у змінній.
    
-   Додана підтримка типу[mixed](language.types.declarations.md#language.types.declarations.mixed)
    
-   Закриті методи, оголошені в батьківському класі, більше не застосовують жодних правил успадкування для методів дочірнього класу (за винятком остаточних закритих конструкторів). У наступному прикладі показано, які обмеження було знято:
    
    ```php
    <?php
    class ParentClass {
        private function method1() {}
        private function method2() {}
        private static function method3() {}
        // Видає попередження, тому що "final" більше не має значення:
        private final function method4() {}
    }
    class ChildClass extends ParentClass {
        // Тепер все наступне дозволено, хоча модифікатори не такі ж,
        // як закритих методів у батьківському класі.
        public abstract function method1() {}
        public static function method2() {}
        public function method3() {}
        public function method4() {}
    }
    ?>
    ```
    
-   Добавлена функция[get\_resource\_id()](function.get-resource-id.md), яка повертає те саме значення, що і`(int) $resource`. Принцип роботи такий самий, але з більш зрозумілим API.
    
-   Добавлен класс[InternalIterator](class.internaliterator.md)
    

### дата та час

-   Були додані[DateTime::createFromInterface()](datetime.createfrominterface.md) і [DateTimeImmutable::createFromInterface()](datetimeimmutable.createfrominterface.md)
    
-   Додано специфікатор формату DateTime`p`, Який аналогічний`P`, але повертає`Z`, а не`+00:00`для UTC.
    

### DOM

Додані [DOMParentNode](class.domparentnode.md) і [DOMChildNode](class.domchildnode.md) з новими API-інтерфейсами обходу та управління.

### Фільтрування даних

**`FILTER_VALIDATE_BOOL`** був доданий як псевдонім для **`FILTER_VALIDATE_BOOLEAN`**. Нове ім'я є доцільним, оскільки воно використовує ім'я канонічного типу.

### Enchant

Додані [enchant\_dict\_add()](function.enchant-dict-add.md) [enchant\_dict\_is\_added()](function.enchant-dict-is-added.md)и\*\*`LIBENCHANT_VERSION`\*\*

### FPM

Добавлена новая опция`pm.status_listen`, що дає змогу отримувати статус з іншої кінцевої точки (наприклад, порту або файлу UDS). Це може стати в нагоді для отримання статусу, коли всі дочірні елементи зайняті обробкою довготривалих запитів.

### Hash

Тепер об'єкти [HashContext](class.hashcontext.md) можна серіалізувати.

### Функції інтернаціоналізації

Додані константи **`IntlDateFormatter::RELATIVE_FULL`** **`IntlDateFormatter::RELATIVE_LONG`** **`IntlDateFormatter::RELATIVE_MEDIUM`** і **`IntlDateFormatter::RELATIVE_SHORT`**

### LDAP

Добавлена функция[ldap\_count\_references()](function.ldap-count-references.md), яка повертає кількість посилань у результатах пошуку.

### OPcache

Якщо ini-параметр opcache.record\_warnings включений, OPcache записуватиме попередження під час компіляції і відтворюватиме їх при наступному включенні, навіть якщо вони обслуговуються з кеша.

### OpenSSL

Додано підтримку синтаксису криптографічних повідомлень (CMS) ([» RFC 5652](http://www.faqs.org/rfcs/rfc5652)), що складається з функцій для шифрування, дешифрування, підпису, перевірки та читання. API схожий на API для функцій PKCS #7 з додаванням нових констант кодування: **`OPENSSL_ENCODING_DER`** **`OPENSSL_ENCODING_SMIME`** і **`OPENSSL_ENCODING_PEM`** :

-   [openssl\_cms\_encrypt()](function.openssl-cms-encrypt.md)шифрує повідомлення у файлі із сертифікатами та виводить результат у наданий файл.
-   [openssl\_cms\_decrypt()](function.openssl-cms-decrypt.md)розшифровує повідомлення S/MIME у файлі та виводить результати у наданий файл.
-   [openssl\_cms\_read()](function.openssl-cms-read.md)експортує файл CMS до масиву сертифікатів PEM.
-   [openssl\_cms\_sign()](function.openssl-cms-sign.md)підписує повідомлення MIME у файлі сертифікатом та ключем та виводить результат у наданий файл.
-   [openssl\_cms\_verify()](function.openssl-cms-verify.md)перевіряє, що блок даних не пошкоджений, сторона, що підписує, є тим, ким вона є і повертає сертифікати сторін, що підписують.

### Регулярні вирази (сумісні з Perl)

Добавлена функция[preg\_last\_error\_msg()](function.preg-last-error-msg.md), яка повертає людину читання повідомлення про останню помилку PCRE. Вона доповнює [preg\_last\_error()](function.preg-last-error.md), яка повертає ціле значення перерахування.

### Reflection

-   Наступні методи тепер можуть повертати інформацію про значення параметрів внутрішніх функцій за промовчанням:
    
    -   [ReflectionParameter::isDefaultValueAvailable()](reflectionparameter.isdefaultvalueavailable.md)
    -   [ReflectionParameter::getDefaultValue()](reflectionparameter.getdefaultvalue.md)
    -   [ReflectionParameter::isDefaultValueConstant()](reflectionparameter.isdefaultvalueconstant.md)
    -   [ReflectionParameter::getDefaultValueConstantName()](reflectionparameter.getdefaultvalueconstantname.md)

### SQLite3

[SQLite3::setAuthorizer()](sqlite3.setauthorizer.md) і відповідні константи класів були додані, за допомогою яких можна встановити власну callback-функцію для авторизації або заборони дії в базі даних.

### Бібліотека стандартних функцій

-   Додані функції [str\_contains()](function.str-contains.md) [str\_starts\_with()](function.str-starts-with.md) і [str\_ends\_with()](function.str-ends-with.md), які перевіряють, чи містить`haystack`, починається або закінчується`needle`соответственно.
    
-   Добавлена функция[fdiv()](function.fdiv.md), яка виконує поділ з плаваючою точкою відповідно до IEEE 754. Поділ на нуль суворо визначено і повертає одне з значень`Inf` `-Inf`или`NaN`
    
-   Добавлена функция[get\_debug\_type()](function.get-debug-type.md)яка повертає тип, який може використовуватися для генерацій повідомлень про помилки. На відміну від[gettype()](function.gettype.md), вона використовує канонічні імена типів, повертає імена класів об'єктів та повідомляє про тип ресурсів.
    
-   [printf()](function.printf.md)та її похідні тепер підтримують специфікатори формату`%h`и`%H`. Вони працюють як`%g`и`%G`, але завжди використовують`"."`як десятковий роздільник, а не визначають його за допомогою локалі\*\*`LC_NUMERIC`\*\*
    
-   [printf()](function.printf.md)та її похідні тепер підтримують використання`"*"`як ширина або точність, і в цьому випадку ширина/точність передається як аргумент printf. Це також дозволяє використовувати точність`-1`с`%g` `%G` `%h`и`%H`. Наприклад, наступний код можна використовувати для відтворення форматування з плаваючою точкою за промовчанням PHP:
    
    ```php
    <?php
    printf("%.*H", (int) ini_get("precision"), $float);
    printf("%.*H", (int) ini_get("serialize_precision"), $float);
    ?>
    ```
    
-   [proc\_open()](function.proc-open.md)Тепер підтримує дескриптори псевдотерміналу (PTY). Наступний код приєднує`stdin` `stdout`и`stderr`до того самого PTY:
    
    ```php
    <?php
    $proc = proc_open($command, [['pty'], ['pty'], ['pty']], $pipes);
    ?>
    ```
    
-   [proc\_open()](function.proc-open.md)Тепер підтримує дескриптори пари сокетів. Наступний код приєднує окрему пару сокетів до`stdin` `stdout`и`stderr` :
    
    ```php
    <?php
    $proc = proc_open($command, [['socket'], ['socket'], ['socket']], $pipes);
    ?>
    ```
    
    На відміну від каналів, у сокетів немає проблем із блокуванням введення-виведення у Windows. Однак не всі програми можуть коректно працювати із сокетами stdio.
    
-   Функції сортування тепер використовують стійке сортування, це означає, що елементи, що порівнюються, збережуть вихідний порядок.
    
-   [array\_diff()](function.array-diff.md) [array\_intersect()](function.array-intersect.md)та їх похідні тепер можуть використовуватися з одним масивом як аргумент. Це означає, що тепер можливе таке:
    
    ```php
    <?php
    // Працює, навіть якщо $excludes порожній:
    array_diff($array, ...$excludes);
    // Працює, навіть якщо $array містить лише один масив:
    array_intersect(...$arrays);
    ?>
    ```
    
-   Параметр`flag` у функції [ob\_implicit\_flush()](function.ob-implicit-flush.md)був змінений, і тепер набуває логічного значення (bool), а не ціле число (int).
    

### Лексер (Tokenizer)

[PhpToken](class.phptoken.md) додає об'єктно-орієнтований інтерфейс до PHP-лексера (tokenizer). Він забезпечує більш одноманітне та ергономічне уявлення, водночас ефективніше та швидше.

### Zip

-   Модуль Zip оновлено до версії 1.19.1.
    
-   Нові методи[ZipArchive::setMtimeName()](ziparchive.setmtimename.md) і [ZipArchive::setMtimeIndex()](ziparchive.setmtimeindex.md)для встановлення часу зміни запису.
    
-   Новий метод [ZipArchive::registerProgressCallback()](ziparchive.registerprogresscallback.md)для надання оновлень під час закриття архіву.
    
-   Новий метод [ZipArchive::registerCancelCallback()](ziparchive.registercancelcallback.md), щоб дозволити скасування під час закриття архіву.
    
-   Новий метод [ZipArchive::replaceFile()](ziparchive.replacefile.md)замінити вміст запису.
    
-   Новий метод [ZipArchive::isCompressionMethodSupported()](ziparchive.iscompressionmethoddupported.md), щоб перевірити додаткові можливості стиснення.
    
-   Новий метод [ZipArchive::isEncryptionMethodSupported()](ziparchive.isencryptionmethoddupported.md), щоб перевірити додаткові функції шифрування.
    
-   Додано властивість ZipArchive::lastId для отримання значення індексу останнього доданого запису.
    
-   Тепер помилки можна перевірити після закриття та за допомогою властивостей ZipArchive::status та ZipArchive::statusSys або методу[ZipArchive::getStatusString()](ziparchive.getstatusstring.md)
    
-   Параметр`'remove_path'`в[ZipArchive::addGlob()](ziparchive.addglob.md) і [ZipArchive::addPattern()](ziparchive.addpattern.md)тепер обробляється як довільний рядковий префікс (для узгодженості з`'add_path'`), тоді як раніше він інтерпретувався як ім'я каталогу.
    
-   Додаткові функції стиснення/шифрування тепер перелічені у phpinfo.

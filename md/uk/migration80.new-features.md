Нова функціональність

-   [« Миграция с PHP 7.4.x на PHP 8.0.x](migration80.html)
    
-   [Изменения, ломающие обратную совместимость »](migration80.incompatible.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.4.x на PHP 8.0.x](migration80.html)
    
-   Нова функціональність
    

## Нова функціональність

### Ядро PHP

#### Іменовані аргументи

Додана підтримка [именованных аргументов](functions.arguments.html#functions.named-arguments)

#### Атрибути

Додана підтримка [атрибутов](language.attributes.html)

#### Оголошення властивостей у конструкторі

Додана підтримка [определения свойств в конструкторе](language.oop5.decon.html#language.oop5.decon.constructor.promotion) (Оголошення властивостей у сигнатурі конструктора).

#### Тип Union

Додана підтримка [объединённых типов](language.types.declarations.html#language.types.declarations.composite.union)

#### Вираз Match

Додана підтримка [выражения `match`](control-structures.match.html)

#### Оператор Nullsafe

Додана підтримка [оператора Nullsafe](language.oop5.basic.html#language.oop5.basic.nullsafe) `?->`

#### Інші нові функції

-   Доданий клас [WeakMap](class.weakmap.html)
    
-   Доданий клас [ValueError](class.valueerror.html)
    
-   Будь-яка кількість параметрів функції тепер може бути замінена варіативним аргументом за сумісності типів. Наприклад, тепер наступний код є допустимим:
    
    ```php
    <?php
    class A {
         public function method(int $many, string $parameters, $here) {}
    }
    class B extends A {
         public function method(...$everything) {}
    }
    ?>
    ```
    
-   static (як у "пізнім статичному зв'язуванні") тепер можна використовувати як тип, що повертається:
    
    ```php
    <?php
    class Test {
         public function create(): static {
              return new static();
         }
    }
    ?>
    ```
    
-   Тепер можна отримати ім'я класу об'єкта за допомогою `$object::class`. Результат такий самий, що й `get_class($object)`
    
-   [`new`](language.oop5.basic.html#language.oop5.basic.new) і [`instanceof`](language.operators.type.html) тепер можна використовувати з довільними виразами, використовуючи `new (expression)(...$args)` і `$obj instanceof (expression)`
    
-   Було внесено деякі виправлення узгодженості до синтаксису змінних, наприклад, тепер дозволено запис `Foo::BAR::$baz`
    
-   Доданий інтерфейс [Stringable](class.stringable.html), який автоматично реалізується, якщо у класі визначено метод [\_\_toString()](language.oop5.magic.html#object.tostring)
    
-   Тепер трейти можуть визначити абстрактні закриті методи. Такі методи мають бути реалізовані класом за допомогою трейту.
    
-   `throw` тепер можна використовувати як вираз. Це означає, що тепер можливе таке:
    
    ```php
    <?php
    $fn = fn() => throw new Exception('Исключение в стрелочной функции');
    $user = $session->user ?? throw new Exception('Должен быть пользователь');
    ```
    
-   У списках параметрів тепер дозволена необов'язкова завершальна кома.
    
    ```php
    <?php
    function functionWithLongSignature(
        Type1 $parameter1,
        Type2 $parameter2, // <-- Эта запятая теперь разрешена.
    ) {
    }
    ```
    
-   Тепер можна написати `catch (Exception)` для перехоплення виключення, не зберігаючи їх у змінній.
    
-   Додана підтримка типу [mixed](language.types.declarations.html#language.types.declarations.mixed)
    
-   Закриті методи, оголошені в батьківському класі, більше не застосовують будь-які правила наслідування для методів дочірнього класу (за винятком остаточних закритих конструкторів). У наступному прикладі показано, які обмеження було знято:
    
    ```php
    <?php
    class ParentClass {
        private function method1() {}
        private function method2() {}
        private static function method3() {}
        // Выдаёт предупреждение, так как "final" больше не имеет значения:
        private final function method4() {}
    }
    class ChildClass extends ParentClass {
        // Теперь все следующее разрешено, хотя модификаторы не такие же,
        // как для закрытых методов в родительском классе.
        public abstract function method1() {}
        public static function method2() {}
        public function method3() {}
        public function method4() {}
    }
    ?>
    ```
    
-   Додана функція [get\_resource\_id()](function.get-resource-id.html), яка повертає те саме значення, що і `(int) $resource`. Принцип роботи такий самий, але з більш зрозумілим API.
    

### дата і час

-   Були додані [DateTime::createFromInterface()](datetime.createfrominterface.html) і [DateTimeImmutable::createFromInterface()](datetimeimmutable.createfrominterface.html)
    
-   Додано специфікатор формату DateTime `p`, Який аналогічний `P`, але повертає `Z`, а не `+00:00` для UTC.
    

### DOM

Додані [DOMParentNode](class.domparentnode.html) і [DOMChildNode](class.domchildnode.html) з новими API-інтерфейсами обходу та управління.

### Фільтрування даних

**`FILTER_VALIDATE_BOOL`** був доданий як псевдонім для **`FILTER_VALIDATE_BOOLEAN`**. Нове ім'я є доцільним, оскільки воно використовує ім'я канонічного типу.

### Enchant

Додані [enchant\_dict\_add()](function.enchant-dict-add.html) [enchant\_dict\_is\_added()](function.enchant-dict-is-added.html) і **`LIBENCHANT_VERSION`**

### FPM

Додана нова опція `pm.status_listen`, що дає змогу отримувати статус з іншої кінцевої точки (наприклад, порту або файлу UDS). Це може стати в нагоді для отримання статусу, коли всі дочірні елементи зайняті обробкою довготривалих запитів.

### Hash

Тепер об'єкти [HashContext](class.hashcontext.html) можна серіалізувати.

### Функції інтернаціоналізації

Додані константи **`IntlDateFormatter::RELATIVE_FULL`** **`IntlDateFormatter::RELATIVE_LONG`** **`IntlDateFormatter::RELATIVE_MEDIUM`** і **`IntlDateFormatter::RELATIVE_SHORT`**

### LDAP

Додана функція [ldap\_count\_references()](function.ldap-count-references.html), яка повертає кількість посилань у результатах пошуку.

### OPcache

Якщо ini-параметр opcache.recordwarnings включений, OPcache записуватиме попередження під час компіляції і відтворюватиме їх при наступному включенні, навіть якщо вони обслуговуються з кеша.

### OpenSSL

Додано підтримку синтаксису криптографічних повідомлень (CMS) ([» RFC 5652](http://www.faqs.org/rfcs/rfc5652)), що складається з функцій для шифрування, дешифрування, підпису, перевірки та читання. API схожий на API для функцій PKCS #7 з додаванням нових констант кодування: **`OPENSSL_ENCODING_DER`** **`OPENSSL_ENCODING_SMIME`** і **`OPENSSL_ENCODING_PEM`**

-   [openssl\_cms\_encrypt()](function.openssl-cms-encrypt.html) шифрує повідомлення у файлі із сертифікатами та виводить результат у наданий файл.
-   [openssl\_cms\_decrypt()](function.openssl-cms-decrypt.html) розшифровує повідомлення S/MIME у файлі та виводить результати у наданий файл.
-   [openssl\_cms\_read()](function.openssl-cms-read.html) експортує файл CMS до масиву сертифікатів PEM.
-   [openssl\_cms\_sign()](function.openssl-cms-sign.html) підписує повідомлення MIME у файлі сертифікатом та ключем та виводить результат у наданий файл.
-   [openssl\_cms\_verify()](function.openssl-cms-verify.html) перевіряє, що блок даних не пошкоджений, сторона, що підписує, є тим, ким вона є і повертає сертифікати сторін, що підписують.

### Регулярні вирази (сумісні з Perl)

Додана функція [preg\_last\_error\_msg()](function.preg-last-error-msg.html), яка повертає людину читання повідомлення про останню помилку PCRE. Вона доповнює [preg\_last\_error()](function.preg-last-error.html), яка повертає ціле значення перерахування.

### Reflection

-   Наступні методи тепер можуть повертати інформацію про значення параметрів внутрішніх функцій за промовчанням:
    
    -   [ReflectionParameter::isDefaultValueAvailable()](reflectionparameter.isdefaultvalueavailable.html)
    -   [ReflectionParameter::getDefaultValue()](reflectionparameter.getdefaultvalue.html)
    -   [ReflectionParameter::isDefaultValueConstant()](reflectionparameter.isdefaultvalueconstant.html)
    -   [ReflectionParameter::getDefaultValueConstantName()](reflectionparameter.getdefaultvalueconstantname.html)

### SQLite3

[SQLite3::setAuthorizer()](sqlite3.setauthorizer.html) і відповідні константи класів були додані, за допомогою яких можна встановити власну callback-функцію для авторизації або заборони дії в базі даних.

### Бібліотека стандартних функцій

-   Додані функції [str\_contains()](function.str-contains.html) [str\_starts\_with()](function.str-starts-with.html) і [str\_ends\_with()](function.str-ends-with.html), які перевіряють, чи містить `haystack`, починається або закінчується `needle` відповідно.
    
-   Додана функція [fdiv()](function.fdiv.html), яка виконує розподіл з плаваючою точкою відповідно до IEEE 754. `Inf` `-Inf` або `NaN`
    
-   Додана функція [get\_debug\_type()](function.get-debug-type.html)яка повертає тип, який може використовуватися для генерацій повідомлень про помилки. На відміну від [gettype()](function.gettype.html), вона використовує канонічні імена типів, повертає імена класів об'єктів та повідомляє про тип ресурсів.
    
-   [printf()](function.printf.html) та її похідні тепер підтримують специфікатори формату `%h` і `%H`. Вони працюють як `%g` і `%G`, але завжди використовують `"."` як десятковий роздільник, а не визначають його за допомогою локалі **`LC_NUMERIC`**
    
-   [printf()](function.printf.html) та її похідні тепер підтримують використання `"*"` як ширина або точність, і в цьому випадку ширина/точність передається як аргумент printf. Це також дозволяє використовувати точність `-1` з `%g` `%G` `%h` і `%H`. Наприклад, наступний код можна використовувати для відтворення форматування з плаваючою точкою за промовчанням PHP:
    
    ```php
    <?php
    printf("%.*H", (int) ini_get("precision"), $float);
    printf("%.*H", (int) ini_get("serialize_precision"), $float);
    ?>
    ```
    
-   [proc\_open()](function.proc-open.html) Тепер підтримує дескриптори псевдотерміналу (PTY). Наступний код приєднує `stdin` `stdout` і `stderr` до того самого PTY:
    
    ```php
    <?php
    $proc = proc_open($command, [['pty'], ['pty'], ['pty']], $pipes);
    ?>
    ```
    
-   [proc\_open()](function.proc-open.html) Тепер підтримує дескриптори пари сокетів. Наступний код приєднує окрему пару сокетів до `stdin` `stdout` і `stderr`
    
    ```php
    <?php
    $proc = proc_open($command, [['socket'], ['socket'], ['socket']], $pipes);
    ?>
    ```
    
    На відміну від каналів, у сокетів немає проблем із блокуванням введення-виведення у Windows. Однак не всі програми можуть коректно працювати із сокетами stdio.
    
-   Функції сортування тепер використовують стійке сортування, це означає, що елементи, що порівнюються, збережуть вихідний порядок.
    
-   [array\_diff()](function.array-diff.html) [array\_intersect()](function.array-intersect.html) та їх похідні тепер можуть використовуватися з одним масивом як аргумент. Це означає, що тепер можливе таке:
    
    ```php
    <?php
    // Работает, даже если $excludes пуст:
    array_diff($array, ...$excludes);
    // Работает, даже если $array содержит только один массив:
    array_intersect(...$arrays);
    ?>
    ```
    
-   Параметр `flag` у функції [ob\_implicit\_flush()](function.ob-implicit-flush.html) був змінений, і тепер набуває логічного значення (bool), а не ціле число (int).
    

### Лексер (Tokenizer)

[PhpToken](class.phptoken.html) додає об'єктно-орієнтований інтерфейс до PHP-лексера (tokenizer). Він забезпечує більш одноманітне та ергономічне уявлення, водночас ефективніше та швидше.

### Zip

-   Модуль Zip оновлено до версії 1.19.1.
    
-   Нові методи [ZipArchive::setMtimeName()](ziparchive.setmtimename.html) і [ZipArchive::setMtimeIndex()](ziparchive.setmtimeindex.html) для встановлення часу зміни запису.
    
-   Новий метод [ZipArchive::registerProgressCallback()](ziparchive.registerprogresscallback.html) для надання оновлень під час закриття архіву.
    
-   Новий метод [ZipArchive::registerCancelCallback()](ziparchive.registercancelcallback.html), щоб дозволити скасування під час закриття архіву.
    
-   Новий метод [ZipArchive::replaceFile()](ziparchive.replacefile.html) замінити вміст запису.
    
-   Новий метод [ZipArchive::isCompressionMethodSupported()](ziparchive.iscompressionmethoddupported.html), щоб перевірити додаткові можливості стиснення.
    
-   Новий метод [ZipArchive::isEncryptionMethodSupported()](ziparchive.isencryptionmethoddupported.html), щоб перевірити додаткові функції шифрування.
    
-   Додано властивість ZipArchive::lastId для отримання значення індексу останнього доданого запису.
    
-   Тепер помилки можна перевірити після закриття та за допомогою властивостей ZipArchive::status та ZipArchive::statusSys або методу [ZipArchive::getStatusString()](ziparchive.getstatusstring.html)
    
-   Параметр `'remove_path'` в [ZipArchive::addGlob()](ziparchive.addglob.html) і [ZipArchive::addPattern()](ziparchive.addpattern.html) тепер обробляється як довільний рядковий префікс (для узгодженості з `'add_path'`), тоді як раніше він інтерпретувався як ім'я каталогу.
    
-   Додаткові функції стиснення/шифрування перераховані в phpinfo.
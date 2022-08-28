Зміни, що ламають зворотну сумісність

-   [« Новая функциональность](migration80.new-features.html)
    
-   [Функциональность, объявленная устаревшей в PHP 8.0.x »](migration80.deprecated.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 7.4.x на PHP 8.0.x](migration80.html)
    
-   Зміни, що ламають зворотну сумісність
    

## Зміни, що ламають зворотну сумісність

### Ядро PHP

#### Порівняння рядків з числами

Нестрогі порівняння чисел і нечислових рядків тепер працюють, як перетворення числа на рядок з наступним порівнянням рядків. Порівняння чисел та числових рядків працює, як і раніше. Зокрема, це означає, що `0 == "not-a-number"` Тепер видасть false.

| Сравнение | До | После |
| --- | --- | --- |
| `0 == "0"` | **`true`** | **`true`** |
| `0 == "0.0"` | **`true`** | **`true`** |
| `0 == "foo"` | **`true`** | **`false`** |
| `0 == ""` | **`true`** | **`false`** |
| `42 == " 42"` | **`true`** | **`true`** |
| `42 == "42foo"` | **`true`** | **`false`** |

#### Інші зміни, що ламають зворотну сумісність

-   `match` тепер зарезервоване ключове слово.
    
-   `mixed` тепер зарезервоване слово, тому його не можна використовувати для назви класу, інтерфейсу чи риси, а також заборонено використовувати у просторах імен.
    
-   Помилки тверджень (assertions) тепер викидаються за умовчанням. Якщо краща стара поведінка, `assert.exception=0` можна встановити в INI-налаштуваннях.
    
-   Методи з тим самим ім'ям, як і клас, більше не інтерпретуються як конструктори. Натомість слід використовувати метод [\_\_construct()](language.oop5.decon.html#object.construct)
    
-   Можливість статичного виклику нестатичних методів видалено. Таким чином, [is\_callable()](function.is-callable.html) завершиться помилкою під час перевірки нестатичного методу з ім'ям класу (необхідно перевіряти з екземпляром об'єкта).
    
-   Приведення типів `(real)` і `(unset)` видалено.
    
-   INI-директива [track\_errors](errorfunc.configuration.html#ini.track-errors) видалено. Це означає, що phperrormsg більше не є актуальним. Замість нього можна використовувати функцію [error\_get\_last()](function.error-get-last.html)
    
-   Можливість визначати константи без урахування регістру було видалено. Третій аргумент [define()](function.define.html) більше не може бути **`true`**
    
-   Можливість вказувати автозавантажувач за допомогою функції [\_\_autoload()](function.autoload.html) було видалено. Натомість слід використовувати [spl\_autoload\_register()](function.spl-autoload-register.html)
    
-   Аргумент `errcontext` більше не передається в користувальницькі обробники помилок, заданих за допомогою [set\_error\_handler()](function.set-error-handler.html)
    
-   [create\_function()](function.create-function.html) було видалено. Замість неї можна використовувати анонімні функції.
    
-   [each()](function.each.html) було видалено. Замість неї можна використовувати [foreach](control-structures.foreach.html) або [ArrayIterator](class.arrayiterator.html)
    
-   Можливість відв'язати це від замикань, які були створені з методу з використанням [Closure::fromCallable()](closure.fromcallable.html) або [ReflectionMethod::getClosure()](reflectionmethod.getclosure.html), було видалено.
    
-   Можливість відв'язати це від належних замикань, що містять використання цього, також була видалена.
    
-   Можливість використання [array\_key\_exists()](function.array-key-exists.html) з об'єктами було видалено. Натомість можна використовувати [isset()](function.isset.html) або [property\_exists()](function.property-exists.html)
    
-   Робота параметра `key` у функції [array\_key\_exists()](function.array-key-exists.html) тепер наведена відповідно до [isset()](function.isset.html) та звичайним доступом до масиву. Всі типи ключів тепер використовують звичайне приведення типів, масив/об'єкт до ключа призведе до викидання [TypeError](class.typeerror.html)
    
-   Будь-який масив, у якого в якості першого числового ключа вказано число n, використовуватиме n+1 для свого наступного неявного ключа, навіть якщо n негативно.
    
-   Рівень errorreporting за замовчуванням тепер **`E_ALL`**. Раніше він виключав **`E_NOTICE`** і **`E_DEPRECATED`**
    
-   [display\_startup\_errors](errorfunc.configuration.html#ini.display-startup-errors) тепер включено за замовчуванням.
    
-   Використання parent всередині класу, який не має батька, тепер призведе до фатальної помилки під час компіляції.
    
-   Оператор `@` більше не пригнічує фатальних помилок (**`E_ERROR`** **`E_CORE_ERROR`** **`E_COMPILE_ERROR`** **`E_USER_ERROR`** **`E_RECOVERABLE_ERROR`** **`E_PARSE`**). Обробники помилок, які очікують, що errorreporting матиме значення `0` при використанні оператора `@`, повинні робити такі перевірки через бітову маску:
    
    ```php
    <?php
    // Замените это
    function my_error_handler($err_no, $err_msg, $filename, $linenum) {
        if (error_reporting() == 0) {
            return false;
        }
        // ...
    }
    
    // На это
    function my_error_handler($err_no, $err_msg, $filename, $linenum) {
        if (!(error_reporting() & $err_no)) {
            return false;
        }
        // ...
    }
    ?>
    ```
    
    Крім цього, обов'язково слід приховати відображення повідомлень про помилки у виробничому середовищі, які можуть призвести до витоку інформації. Перевірте, що `display_errors=Off` використовується разом із записом журналу помилок.
    
-   `#[` більше не інтерпретується як початок коментаря, оскільки цей синтаксис тепер використовується для атрибутів.
    
-   Помилки успадкування через несумісні сигнатури методів (порушення LSP) тепер завжди викликають фатальну помилку. Раніше у деяких випадках видавалося попередження.
    
-   Пріоритет оператора конкатенації змінився щодо зрушень бітів і додавання, а також віднімання.
    
    ```php
    <?php
    echo "Сумма: " . $a + $b;
    // ранее интерпретировалось как:
    echo ("Сумма: " . $a) + $b;
    // сейчас интерпретируется как:
    echo "Сумма:" . ($a + $b);
    ?>
    ```
    
-   Аргументи зі значенням за замовчуванням, що перетворюється на **`null`** під час виконання, більше не будуть явно позначати тип аргументу як nullable. Натомість має використовуватися або явний тип, що допускає значення null, або явне значення **`null`** за замовчуванням.
    
    ```php
    <?php
    // Замените этот код:
    function test(int $arg = CONST_RESOLVING_TO_NULL) {}
    // На этот:
    function test(?int $arg = CONST_RESOLVING_TO_NULL) {}
    // На этот (альтернативный вариант):
    function test(int $arg = null) {}
    ?>
    ```
    
-   Ряд попереджень перетворено на винятки [Error](class.error.html)
    
    -   Спроба запису як неіснуючого об'єкта. Раніше це неявно створювало об'єкт stdClass у разі null, false та порожніх рядків.
    -   Спроба додати елемент до масиву, для якого вже використовується ключ PHPINTMAX.
    -   Спроба використовувати неприпустимий тип (масив або об'єкт) як ключ масиву або зміщення рядка.
    -   Спроба записати в індекс масиву скалярне значення.
    -   Спроба розпакувати значення, яке не є масивом/Traversable.
    -   Спроба отримати доступ до некваліфікованих константів, які не визначені. Раніше некваліфікований доступ до константів призводив до попередження та інтерпретувався як рядок.
    
    Ряд повідомлень перетворено на попередження:
    
    -   Спроба прочитати невизначену змінну.
    -   Спроба прочитати невизначену властивість.
    -   Спроба прочитати невизначений ключ масиву.
    -   Спроба прочитати властивість необ'єкта.
    -   Спроба отримати доступ до індексу масиву немасиву.
    -   Спроба перетворити масив на рядок.
    -   Спроба використовувати ресурс як ключ масиву.
    -   Спроба використовувати null, логічне значення чи число з плаваючою точкою як рядковий зсув.
    -   Спроба прочитати усунення рядка за межами допустимого кордону.
    -   Спроба присвоїти зміщення рядка порожній рядок.
-   При спробі призначити кілька байтів усунення рядка тепер буде видано попередження.
    
-   Несподівані символи у вихідних файлах (наприклад, байти NUL за межами рядків) тепер призводять до виключення [ParseError](class.parseerror.html) замість попередження під час компіляції.
    
-   Неперехоплені винятки тепер проходять процедуру "чистого завершення", це означає, що після неперехопленого виключення викликатимуться деструктори.
    
-   Фатальна помилка часу компіляції "Only variables can be passed by reference" була відкладена до часу виконання та перетворена на виключення [Error](class.error.html) "Argument cannot be passed by reference".
    
-   Деякі повідомлення "Only variables can be passed by reference" були перетворені на виключення "Argument cannot be passed by reference".
    
-   Згенероване ім'я для анонімних класів змінилося. Тепер він буде включати ім'я першого з батьків або інтерфейсу:
    
    ```php
    <?php
    new class extends ParentClass {};
    // -> ParentClass@anonymous
    new class implements FirstInterface, SecondInterface {};
    // -> FirstInterface@anonymous
    new class {};
    // -> class@anonymous
    ?>
    ```
    
    За новими іменами, як і раніше, слідуватиме NUL-байт і унікальний суфікс.
    
-   Посилання на неабсолютні трейти методів в адаптаціях псевдонімів трейтів мають бути однозначними:
    
    ```php
    <?php
    class X {
        use T1, T2 {
            func as otherFunc;
        }
        function func() {}
    }
    ?>
    ```
    
    Якщо існують і `T1::func()`, і `T2::func()`, цей код раніше приймався без повідомлення, і передбачалося, що func посилається на `T1::func`. Тепер натомість буде викинуто фатальну помилку: необхідно явно вказати `T1::func` або `T2::func`
    
-   Сигнатура абстрактних методів, визначених у трейтах, тепер перевіряється за методом класу, що реалізує:
    
    ```php
    <?php
    trait MyTrait {
        abstract private function neededByTrait(): string;
    }
    
    class MyClass {
        use MyTrait;
    
        // Ошибка из-за несоответствия типа возвращаемого значения.
        private function neededByTrait(): int { return 42; }
    }
    ?>
    ```
    
-   Відключені функції тепер обробляються так само, як неіснуючі функції. Виклик вимкненої функції повідомить, що немає такої функції, це дає можливість перевизначити вимкнену функцію.
    
-   Оболонки потоку `data://` більше не доступні для запису, що відповідає документованій поведінці.
    
-   Арифметичні та побітові оператори `+` `-` `*` `/` `**` `%` `<<` `>>` `&` `|` `^` `~` `++` `--` тепер будуть послідовно видавати [TypeError](class.typeerror.html), коли одним з операндів є масив (array), ресурс ([resource](language.types.resource.html)) чи не перевантажений об'єкт (object). Єдиним винятком із цього правила є операція злиття масивів `+`яка, як і раніше, підтримується.
    
-   Приведення з плаваючою точкою в рядок тепер завжди поводитиметься незалежно від локалі.
    
    ```php
    <?php
    setlocale(LC_ALL, "de_DE");
    // Ранее:  3,14
    // Теперь: 3.14
    ?>
    ```
    
    Дивіться [printf()](function.printf.html) [number\_format()](function.number-format.html) і **NumberFormatter()** для отримання інформації про способи настроювання форматування чисел.
    
-   Видалено підтримку застарілих фігурних дужок для доступу до зміщення.
    
    ```php
    <?php
    // Вместо:
    $array{0};
    $array{"key"};
    // Используйте:
    $array[0];
    $array["key"];
    ?>
    ```
    
-   Застосування модифікатора final до закритого методу тепер спричинить попередження, якщо цей метод не є конструктором.
    
-   Якщо у конструкторі об'єкта використовується [exit()](function.exit.html), Деструктор об'єкта більше не буде викликатися. Це відповідає поведінці, коли конструктор викидає виняток.
    
-   Імена у просторі імен більше не можуть містити прогалини: `Foo\Bar` буде розпізнаватись як ім'я в просторі імен, `Foo \ Bar` - Ні. І навпаки, зарезервовані ключові слова тепер дозволені як сегменти простору імен, що також може змінити інтерпретацію коду: `new\x` тепер збігається з `constant('new\x')`, але не з `new \x()`
    
-   Для вкладених тернарних операторів тепер потрібна явна вказівка ​​дужок.
    
-   [debug\_backtrace()](function.debug-backtrace.html) і [Exception::getTrace()](exception.gettrace.html) більше не надаватимуть посилання на аргументи. Неможливо змінити аргументи функції через трасування.
    
-   Обробка числових рядків була змінена, щоб зробити її більш зрозумілою і менш схильною до помилок. Завершальні прогалини тепер дозволено у числових рядках для узгодженості з тим, як обробляються початкові прогалини. В основному це впливає на:
    
    -   функцію [is\_numeric()](function.is-numeric.html)
    -   Порівняння рядків з рядками
    -   Оголошення типів
    -   Операції збільшення та зменшення
    
    Поняття "провідний числовий рядок" в основному було відкинуто; випадки, коли це залишилося, є для полегшення міграції. Рядки, які видавали **`E_NOTICE`** "A non well-formed numeric value encountered", тепер видаватимуть **`E_WARNING`** "A non-numeric value encountered", а всі рядки, які видавали **`E_WARNING`** "A non-numeric value encountered" тепер видаватиме [TypeError](class.typeerror.html). В основному це впливає на:
    
    -   Арифметичні операції
    -   Побітові операції
    
    Ця зміна **`E_WARNING`** на [TypeError](class.typeerror.html) також впливає на **`E_WARNING`** "Illegal string offset 'string'" для неприпустимих зсувів рядка. Поведінка явних наведень до int/float з рядків не змінилася.
    
-   Тепер у магічних методів перевірятимуться аргументи і типи, що повертаються, якщо вони оголошені. Сигнатура має відповідати наступному списку:
    
    -   `__call(string $name, array $arguments): mixed`
    -   `__callStatic(string $name, array $arguments): mixed`
    -   `__clone(): void`
    -   `__debugInfo(): ?array`
    -   `__get(string $name): mixed`
    -   `__invoke(mixed $arguments): mixed`
    -   `__isset(string $name): bool`
    -   `__serialize(): array`
    -   `__set(string $name, mixed $value): void`
    -   `__set_state(array $properties): object`
    -   `__sleep(): array`
    -   `__unserialize(array $data): void`
    -   `__unset(string $name): void`
    -   `__wakeup(): void`
-   Ключі масиву [call\_user\_func\_array()](function.call-user-func-array.html) тепер інтерпретуватимуться як імена параметрів, а не ігноруватимуться.
    
-   Оголошення функції з ім'ям `assert()` всередині простору імен більше не допускається та викликає **`E_COMPILE_ERROR`**. Функція [assert()](function.assert.html) піддається спеціальної обробки з боку движка, що може призвести до неузгодженої поведінки щодо однойменної функції у просторі імен.
    

### Перетворення ресурсів на об'єкти

Декілька ресурсів ([resource](language.types.resource.html)) були перетворені на об'єкти (object). Перевірки значення, що повертається з використанням [is\_resource()](function.is-resource.html) слід замінити перевірками на **`false`**

-   [curl\_init()](function.curl-init.html) тепер повертає об'єкт [CurlHandle](class.curlhandle.html) замість ресурсу ([resource](language.types.resource.html)). Функція [curl\_close()](function.curl-close.html) більше не має сенсу, натомість екземпляр [CurlHandle](class.curlhandle.html) автоматично знищується, якщо на нього немає посилання.
    
-   [curl\_multi\_init()](function.curl-multi-init.html) тепер повертає об'єкт [CurlMultiHandle](class.curlmultihandle.html) замість ресурсу ([resource](language.types.resource.html)). Функція [curl\_multi\_close()](function.curl-multi-close.html) більше не має сенсу, натомість екземпляр [CurlMultiHandle](class.curlmultihandle.html) автоматично знищується, якщо на нього немає посилання.
    
-   [curl\_share\_init()](function.curl-share-init.html) тепер повертає об'єкт [CurlShareHandle](class.curlsharehandle.html) замість ресурсу ([resource](language.types.resource.html)). Функція [curl\_share\_close()](function.curl-share-close.html) більше не має сенсу, натомість екземпляр [CurlShareHandle](class.curlsharehandle.html) автоматично знищується, якщо на нього немає посилання.
    
-   [enchant\_broker\_init()](function.enchant-broker-init.html) тепер повертає об'єкт [EnchantBroker](class.enchantbroker.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [enchant\_broker\_request\_dict()](function.enchant-broker-request-dict.html) і [enchant\_broker\_request\_pwl\_dict()](function.enchant-broker-request-pwl-dict.html) тепер повертають [EnchantDictionary](class.enchantdictionary.html) об'єкт замість ресурсу ([resource](language.types.resource.html)
    
-   Модуль GD тепер використовує об'єкти [GdImage](class.gdimage.html) як базова структура даних для зображень, а не ресурси ([resource](language.types.resource.html)). Функція [imagedestroy()](function.imagedestroy.html) більше немає сенсу; натомість екземпляр [GdImage](class.gdimage.html) автоматично знищується, якщо на нього немає посилання.
    
-   [openssl\_x509\_read()](function.openssl-x509-read.html) і [openssl\_csr\_sign()](function.openssl-csr-sign.html) тепер повертають об'єкт [OpenSSLCertificate](class.opensslcertificate.html) замість ресурсу ([resource](language.types.resource.html)). Функція [openssl\_x509\_free()](function.openssl-x509-free.html) оголошена застарілою і більше не має сенсу, натомість екземпляр [OpenSSLCertificate](class.opensslcertificate.html) автоматично знищується, якщо на нього більше не посилаються.
    
-   [openssl\_csr\_new()](function.openssl-csr-new.html) тепер повертає об'єкт [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [openssl\_pkey\_new()](function.openssl-pkey-new.html) тепер повертає об'єкт [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) замість ресурсу ([resource](language.types.resource.html)). Функція [openssl\_pkey\_free()](function.openssl-pkey-free.html) оголошена застарілою і більше не має сенсу, натомість екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) автоматично знищується, якщо на нього більше не посилаються.
    
-   [shmop\_open()](function.shmop-open.html) тепер повертає об'єкт [Shmop](class.shmop.html) замість ресурсу ([resource](language.types.resource.html)). Функція [shmop\_close()](function.shmop-close.html) більше немає сенсу і оголошена застарілою; натомість екземпляр [Shmop](class.shmop.html) автоматично знищується, якщо на нього більше не посилаються.
    
-   [socket\_create()](function.socket-create.html) [socket\_create\_listen()](function.socket-create-listen.html) [socket\_accept()](function.socket-accept.html) [socket\_import\_stream()](function.socket-import-stream.html) [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.html) [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html) і [socket\_wsaprotocol\_info\_import()](function.socket-wsaprotocol-info-import.html) тепер повертають об'єкт [Socket](class.socket.html) замість ресурсу ([resource](language.types.resource.html) . [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html) тепер повертає масив об'єктів [AddressInfo](class.addressinfo.html) замість масиву ресурсів ([resource](language.types.resource.html)
    
-   [msg\_get\_queue()](function.msg-get-queue.html) тепер повертають об'єкт [SysvMessageQueue](class.sysvmessagequeue.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [sem\_get()](function.sem-get.html) тепер повертають об'єкт [SysvSemaphore](class.sysvsemaphore.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [shm\_attach()](function.shm-attach.html) тепер повертають об'єкт [SysvSharedMemory](class.sysvsharedmemory.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [xml\_parser\_create()](function.xml-parser-create.html) і [xml\_parser\_create\_ns()](function.xml-parser-create-ns.html) тепер повертають об'єкт [XMLParser](class.xmlparser.html) замість ресурсу ([resource](language.types.resource.html)). Функція [xml\_parser\_free()](function.xml-parser-free.html) більше не має сенсу, натомість екземпляр XMLParser автоматично знищується, якщо на нього більше не посилаються.
    
-   Функції [XMLWriter](book.xmlwriter.html) тепер приймають та повертають, відповідно, об'єкти [XMLWriter](class.xmlwriter.html) замість ресурсів ([resource](language.types.resource.html)
    
-   [inflate\_init()](function.inflate-init.html) тепер повертає об'єкт [InflateContext](class.inflatecontext.html) замість ресурсу ([resource](language.types.resource.html)
    
-   [deflate\_init()](function.deflate-init.html) тепер повертає об'єкт [DeflateContext](class.deflatecontext.html) замість ресурсу ([resource](language.types.resource.html)
    

### COM та .Net (Windows)

Можливість імпорту констант без урахування регістру з бібліотек типів було видалено. Другий аргумент [com\_load\_typelib()](function.com-load-typelib.html) більше не може бути false; [com.autoregister\_casesensitive](com.configuration.html#ini.com.autoregister-casesensitive) більше не можна вимкнути; Маркери без урахування регістру в [com.typelib\_file](com.configuration.html#ini.com.typelib-file) ігноруються.

### CURL

**`CURLOPT_POSTFIELDS`** більше не сприймає об'єкти як масиви. Щоб інтерпретувати об'єкт як масив, виконайте явне приведення `(array)`. Те саме стосується й інших параметрів, що приймають масиви.

### дата і час

Для роботи функцій [mktime()](function.mktime.html) і [gmmktime()](function.gmmktime.html) тепер потрібно хоча б один аргумент . [time()](function.time.html) може використовуватись для отримання поточної позначки часу.

### DOM

Були видалені нереалізовані класи з модуля DOM, які мали обробника і містили тестові дані. Ці класи також були видалені в останній версії стандарту DOM:

-   **DOMNameList**
-   **DomImplementationList**
-   **DOMConfiguration**
-   **DomError**
-   **DomErrorHandler**
-   **DOMImplementationSource**
-   **DOMLocator**
-   **DOMUserDataHandler**
-   **DOMTypeInfo**
-   **DOMStringExtend**

Видалено нереалізовані методи модуля DOM, які не мали реалізації:

-   **DOMNamedNodeMap::setNamedItem()**
-   **DOMNamedNodeMap::removeNamedItem()**
-   **DOMNamedNodeMap::setNamedItemNS()**
-   **DOMNamedNodeMap::removeNamedItemNS()**
-   **DOMText::replaceWholeText()**
-   **DOMNode::compareDocumentPosition()**
-   **DOMNode::isEqualNode()**
-   **DOMNode::getFeature()**
-   **DOMNode::setUserData()**
-   **DOMNode::getUserData()**
-   **DOMDocument::renameNode()**

### Enchant

-   [enchant\_broker\_list\_dicts()](function.enchant-broker-list-dicts.html) [enchant\_broker\_describe()](function.enchant-broker-describe.html) і [enchant\_dict\_suggest()](function.enchant-dict-suggest.html) тепер повертають порожній масив замість **`null`**

### Exif

[read\_exif\_data()](function.read-exif-data.html) була видалена; Замість неї слід використовувати [exif\_read\_data()](function.exif-read-data.html)

### Фільтрування даних

-   Прапори **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** для фільтра **`FILTER_VALIDATE_URL`** були видалені . `scheme` і `host` необхідні (і завжди були).
    
-   Типи **`INPUT_REQUEST`** і **`INPUT_SESSION`** для [filter\_input()](function.filter-input.html) та її похідних були видалені. Вони ніколи не були реалізовані, а спроба їх використання завжди викликала попередження.
    

### ДД

-   Застарілі функції [image2wbmp()](function.image2wbmp.html) були вилучені.
    
-   Застарілі функції [png2wbmp()](function.png2wbmp.html) і [jpeg2wbmp()](function.jpeg2wbmp.html) були вилучені.
    
-   Параметр `mode` за замовчуванням для функції [imagecropauto()](function.imagecropauto.html) більше не набуває значення `-1`. Натомість слід використовувати **`IMG_CROP_DEFAULT`**
    
-   У Windows, phpgd2.dll перейменований на phpgd.dll
    

### GMP

[gmp\_random()](function.gmp-random.html) було видалено. Замість неї слід використовувати [gmp\_random\_range()](function.gmp-random-range.html) або [gmp\_random\_bits()](function.gmp-random-bits.html)

### Iconv

Реалізації iconv, які неправильно встановлюють errno у разі виникнення помилок, більше не підтримуються.

### IMAP

-   Невикористовуваний аргумент `default_host` функції [imap\_headerinfo()](function.imap-headerinfo.html) був видалений.
    
-   Функція [imap\_header()](function.imap-header.html)яка є псевдонімом [imap\_headerinfo()](function.imap-headerinfo.html), було видалено.
    

### Функції інтернаціоналізації

-   Застаріла константа **`INTL_IDNA_VARIANT_2003`** видалено.
    
-   Застаріла константа **`Normalizer::NONE`** видалено.
    

### LDAP

-   Застарілі функції [ldap\_sort()](function.ldap-sort.html) [ldap\_control\_paged\_result()](function.ldap-control-paged-result.html) і [ldap\_control\_paged\_result\_response()](function.ldap-control-paged-result-response.html) видалено.
    
-   Змінився інтерфейс [ldap\_set\_rebind\_proc()](function.ldap-set-rebind-proc.html); параметр `callback` більше не приймає порожні рядки; натомість слід вказувати **`null`**
    

### MBString

-   Директива [mbstring.func\_overload](mbstring.configuration.html#ini.mbstring.func-overload) було видалено. Пов'язані константи **`MB_OVERLOAD_MAIL`** **`MB_OVERLOAD_STRING`** і **`MB_OVERLOAD_REGEX`** також було видалено. Зрештою, записи `"func_overload"` і `"func_overload_list"` в [mb\_get\_info()](function.mb-get-info.html) були вилучені.
    
-   [mb\_parse\_str()](function.mb-parse-str.html) більше не можна використовувати без передачі масиву результатів.
    
-   Видалено низку застарілих псевдонімів mbregex. У наступному списку вказано, які функції слід використовувати замість них:
    
    -   **mbregexencoding()** [mb\_regex\_encoding()](function.mb-regex-encoding.html)
    -   **mbereg()** [mb\_ereg()](function.mb-ereg.html)
    -   **mberegi()** [mb\_eregi()](function.mb-eregi.html)
    -   **mberegreplace()** [mb\_ereg\_replace()](function.mb-ereg-replace.html)
    -   **mberegireplace()** [mb\_eregi\_replace()](function.mb-eregi-replace.html)
    -   **mbsplit()** [mb\_split()](function.mb-split.html)
    -   **mberegmatch()** [mb\_ereg\_match()](function.mb-ereg-match.html)
    -   **mberegsearch()** [mb\_ereg\_search()](function.mb-ereg-search.html)
    -   **mberegsearchpos()** [mb\_ereg\_search\_pos()](function.mb-ereg-search-pos.html)
    -   **mberegsearchregs()** [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.html)
    -   **mberegsearchinit()** [mb\_ereg\_search\_init()](function.mb-ereg-search-init.html)
    -   **mberegsearchgetregs()** [mb\_ereg\_search\_getregs()](function.mb-ereg-search-getregs.html)
    -   **mberegsearchgetpos()** [mb\_ereg\_search\_getpos()](function.mb-ereg-search-getpos.html)
    -   **mberegsearchsetpos()** [mb\_ereg\_search\_setpos()](function.mb-ereg-search-setpos.html)
-   Модифікатор `e` для [mb\_ereg\_replace()](function.mb-ereg-replace.html) був видалений. Замість нього слід використовувати[mb\_ereg\_replace\_callback()](function.mb-ereg-replace-callback.html)
    
-   Аргумент нерядкового шаблону для [mb\_ereg\_replace()](function.mb-ereg-replace.html) тепер інтерпретуватиметься як рядок замість кодової точки ASCII. Попередню поведінку можна відновити явним викликом [chr()](function.chr.html)
    
-   Аргумент `needle` для функцій [mb\_strpos()](function.mb-strpos.html) [mb\_strrpos()](function.mb-strrpos.html) [mb\_stripos()](function.mb-stripos.html) [mb\_strripos()](function.mb-strripos.html) [mb\_strstr()](function.mb-strstr.html) [mb\_stristr()](function.mb-stristr.html) [mb\_strrchr()](function.mb-strrchr.html) і [mb\_strrichr()](function.mb-strrichr.html) тепер може бути порожнім.
    
-   Параметр `is_hex`, який не використовувався для внутрішніх цілей, був видалений з [mb\_decode\_numericentity()](function.mb-decode-numericentity.html)
    
-   Застаріла поведінка передачі кодування як третій аргумент замість зміщення функції [mb\_strrpos()](function.mb-strrpos.html) було видалено; замість цього як четвертий аргумент слід вказати явне зміщення `0` з кодуванням.
    
-   Псевдоніми кодування символів `ISO_8859-*` були замінені на псевдоніми `ISO8859-*` для кращої сумісності із модулем iconv. Псевдоніми mbregex ISO 8859 з підкресленням (`ISO_8859_*` і `ISO8859_*`) також були видалені.
    
-   [mb\_ereg()](function.mb-ereg.html) і [mb\_eregi()](function.mb-eregi.html) тепер повертатимуть логічне значення **`true`**, у разі знайденого збігу. Раніше вони повертали ціле число `1`, якщо аргумент `matches` не було передано, або `max(1, strlen($matches[0]))`, якщо `matches` був не пустий.
    

### OCI8

-   Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html), а клас **OCI-Collection** - у [OCICollection](class.ocicollection.html) для імені сумісність забезпечується засобами інструкції типу arginfo PHP 8.
    
-   Деякі функції псевдонімів оголошено застарілим.
    
-   [oci\_internal\_debug()](function.oci-internal-debug.html) та її псевдонім [ociinternaldebug()](function.ociinternaldebug.html) були вилучені.
    

### ODBC

-   [odbc\_connect()](function.odbc-connect.html) більше не використовує з'єднання повторно.
    
-   Параметр, що не використовується `flags` функції [odbc\_exec()](function.odbc-exec.html) був видалений.
    

### OpenSSL

-   [openssl\_seal()](function.openssl-seal.html) і [openssl\_open()](function.openssl-open.html) тепер вимагають передачі `method`, так як попереднє значення за замовчуванням `"RC4"` вважається небезпечним.

### Регулярні вирази (сумісні з Perl)

При передачі неприпустимих послідовностей, що управляють, вони більше не інтерпретуються як літерали. Така поведінка раніше вимагала модифікатора `X`, що тепер ігнорується.

### Об'єкти даних PHP

-   Режим обробки помилок за умовчанням було змінено з "тихого" (silent) на "виключення" (exceptions). Детальніше дивіться [Ошибки и обработка ошибок](pdo.error-handling.html)
    
-   Змінилися сигнатури деяких методів PDO:
    
    -   `PDO::query(string $query, ?int $fetchMode = null, mixed ...$fetchModeArgs)`
    -   `PDOStatement::setFetchMode(int $mode, mixed ...$args)`

### PDO ODBC

Директива php.ini [pdo\_odbc.db2\_instance\_name](ref.pdo-odbc.html#ini.pdo-odbc.db2-instance-name) було видалено.

### PDO MySQL

[PDO::inTransaction()](pdo.intransaction.html) тепер повідомляє фактичний стан транзакції підключення, а не про приблизний від PDO. Якщо запит, за умови "неявної фіксації", виконується, то [PDO::inTransaction()](pdo.intransaction.html) згодом поверне **`false`**, оскільки транзакція буде неактивною.

### PostgreSQL

-   Застарілий синтаксис [pg\_connect()](function.pg-connect.html) за допомогою кількох параметрів замість рядка підключення більше не підтримується.
    
-   Застарілі сигнатури [pg\_lo\_import()](function.pg-lo-import.html) і [pg\_lo\_export()](function.pg-lo-export.html), що передають з'єднання як останній аргумент, більше не підтримуються. Натомість з'єднання має бути передано першим аргументом.
    
-   [pg\_fetch\_all()](function.pg-fetch-all.html) тепер повертатиме порожній масив замість **`false`** для наборів результатів із відсутніми рядками.
    

### Phar

Метадані, пов'язані з phar, більше не будуть автоматично десеріалізуватися, щоб виправити потенційні вразливості безпеки через створення екземплярів об'єкта, автозавантаження тощо.

### Reflection

-   Сигнатури методів
    
    -   `ReflectionClass::newInstance($args)`
    -   `ReflectionFunction::invoke($args)`
    -   `ReflectionMethod::invoke($object, $args)`
    
    були змінені на:
    
    -   `ReflectionClass::newInstance(...$args)`
    -   `ReflectionFunction::invoke(...$args)`
    -   `ReflectionMethod::invoke($object, ...$args)`
    
    Код, який повинен бути сумісний як з PHP 7, так і з PHP 8, може використовувати такі сигнатури:
    
    -   `ReflectionClass::newInstance($arg = null, ...$args)`
    -   `ReflectionFunction::invoke($arg = null, ...$args)`
    -   `ReflectionMethod::invoke($object, $arg = null, ...$args)`
-   Метод [ReflectionType::\_\_toString()](reflectiontype.tostring.html) тепер повертатиме повне налагоджувальне уявлення типу і більше не є застарілим. Зокрема, результат включатиме індикатор допустимості значень NULL для типів, що допускають значення NULL. Формат значення, що повертається, нестабільний і може змінюватися в залежності від версії PHP.
    
-   Методи Reflection export() були видалені. Натомість об'єкти reflection можуть бути перетворені на рядок.
    
-   [ReflectionMethod::isConstructor()](reflectionmethod.isconstructor.html) і [ReflectionMethod::isDestructor()](reflectionmethod.isdestructor.html) тепер також повертають **`true`** для методів інтерфейсів [\_\_construct()](language.oop5.decon.html#object.construct) і [\_\_destruct()](language.oop5.decon.html#object.destruct). Раніше це було вірно лише для методів класів та трейтів.
    
-   Метод **ReflectionType::isBuiltin()** переміщений у [ReflectionNamedType](class.reflectionnamedtype.html). У [ReflectionUnionType](class.reflectionuniontype.html) цього методу немає.
    

### Сокети

-   Застарілі `flags` **`AI_IDN_ALLOW_UNASSIGNED`** і **`AI_IDN_USE_STD3_ASCII_RULES`** для [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html) були вилучені.

### Стандартна бібліотека PHP (SPL)

-   [SplFileObject::fgetss()](splfileobject.fgetss.html) був видалений.
    
-   [SplFileObject::seek()](splfileobject.seek.html) тепер завжди переміщається початку рядка. Раніше, позиція `>=1` переміщала на початок наступні рядки.
    
-   [SplHeap::compare()](splheap.compare.html) тепер вказує сигнатуру методу. Наслідуючі класи, які реалізують цей метод, тепер повинні використовувати сумісну сигнатуру методу.
    
-   [SplDoublyLinkedList::push()](spldoublylinkedlist.push.html) [SplDoublyLinkedList::unshift()](spldoublylinkedlist.unshift.html) і [SplQueue::enqueue()](splqueue.enqueue.html) тепер повертають void замість **`true`**
    
-   [spl\_autoload\_register()](function.spl-autoload-register.html) тепер завжди викидатиме [TypeError](class.typeerror.html) для неприпустимих аргументів, тому другий аргумент `do_throw` ігнорується, якщо для нього встановлено значення **`false`**
    
-   [SplFixedArray](class.splfixedarray.html) тепер є [IteratorAggregate](class.iteratoraggregate.html), а не [Iterator](class.iterator.html). . [SplFixedArray::rewind()](splfixedarray.rewind.html) [SplFixedArray::current()](splfixedarray.current.html) [SplFixedArray::key()](splfixedarray.key.html) [SplFixedArray::next()](splfixedarray.next.html) і [SplFixedArray::valid()](splfixedarray.valid.html) були вилучені. Замість них було додано **SplFixedArray::getIterator()**. Будь-який код, який використовує явну ітерацію над SplFixedArray, тепер має отримати [Iterator](class.iterator.html) за допомогою **SplFixedArray::getIterator()**. Це означає, що [SplFixedArray](class.splfixedarray.html) тепер безпечно використовувати у вкладених циклах.
    

### Бібліотека стандартних функцій

-   [assert()](function.assert.html) більше не виконуватиме рядкові аргументи, натомість вони будуть оброблятися як будь-які звичайні аргументи. Таким чином, замість `assert('$a == $b')` слід використовувати `assert($a == $b)`. INI-директива [assert.quiet\_eval](info.configuration.html#ini.assert.quiet-eval) та константа **`ASSERT_QUIET_EVAL`** були видалені, оскільки вони не мають сенсу.
    
-   [parse\_str()](function.parse-str.html) більше не можна використовувати без зазначення масиву результатів.
    
-   Фільтр [string.strip\_tags](filters.string.html#filters.string.strip_tags) видалено.
    
-   Аргумент `needle` функцій [strpos()](function.strpos.html) [strrpos()](function.strrpos.html) [stripos()](function.stripos.html) [strripos()](function.strripos.html) [strstr()](function.strstr.html) [strchr()](function.strchr.html) [strrchr()](function.strrchr.html) і [stristr()](function.stristr.html) тепер завжди інтерпретуватиметься як рядок. Раніше невеликі потреби інтерпретувалися як кодова точка ASCII. Явний виклик [chr()](function.chr.html) може використовуватись для відновлення попередньої поведінки.
    
-   Аргумент `needle` функцій [strpos()](function.strpos.html) [strrpos()](function.strrpos.html) [stripos()](function.stripos.html) [strripos()](function.strripos.html) [strstr()](function.strstr.html) [stristr()](function.stristr.html) і [strrchr()](function.strrchr.html) тепер може бути порожнім.
    
-   Аргумент `length` функцій [substr()](function.substr.html) [substr\_count()](function.substr-count.html) [substr\_compare()](function.substr-compare.html) і [iconv\_substr()](function.iconv-substr.html) тепер може бути **`null`**. Значення **`null`** означає відсутність аргументу довжини, і тому функції повернуть залишок рядка замість порожнього рядка.
    
-   Аргумент `length` функції [array\_splice()](function.array-splice.html) тепер може бути **`null`**. Передача значення **`null`** означає відсутність аргументу, тому функція видалити все, починаючи від `offset` до кінця масиву.
    
-   Аргумент `args` функцій [vsprintf()](function.vsprintf.html) [vfprintf()](function.vfprintf.html) і [vprintf()](function.vprintf.html) тепер має бути масивом. Раніше приймався будь-який тип.
    
-   Параметр `'salt'` функції [password\_hash()](function.password-hash.html) більше не підтримується. Якщо використовується опція `'salt'`, генерується попередження, передана сіль ігнорується, а замість неї використовується сгенерована сіль.
    
-   Функція [quotemeta()](function.quotemeta.html) тепер повертатиме порожній рядок, якщо було передано порожній рядок. Раніше поверталося **`false`**
    
-   Видалено такі функції:
    
    -   [hebrevc()](function.hebrevc.html)
    -   [convert\_cyr\_string()](function.convert-cyr-string.html)
    -   [money\_format()](function.money-format.html)
    -   [ezmlm\_hash()](function.ezmlm-hash.html)
    -   [restore\_include\_path()](function.restore-include-path.html)
    -   [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.html)
    -   [get\_magic\_quotes\_runtime()](function.get-magic-quotes-runtime.html)
    -   [fgetss()](function.fgetss.html)
-   **`FILTER_SANITIZE_MAGIC_QUOTES`** видалено.
    
-   Виклик [implode()](function.implode.html) з параметрами у зворотному порядку `($pieces, $glue)` більше не підтримується.
    
-   [parse\_url()](function.parse-url.html) тепер буде розрізняти відсутні та порожні запити та фрагменти:
    
    -   `http://example.com/foo → query = null, fragment = null`
    -   `http://example.com/foo? → query = "", fragment = null`
    -   `http://example.com/foo# → query = null, fragment = ""`
    -   `http://example.com/foo?# → query = "", fragment = ""`
    
    Раніше у всіх випадках query та fragment були **`null`**
    
-   [var\_dump()](function.var-dump.html) і [debug\_zval\_dump()](function.debug-zval-dump.html) тепер друкуватимуть числа з плаваючою точкою, використовуючи [serialize\_precision](ini.core.html#ini.serialize-precision), а не [precision](ini.core.html#ini.precision). У конфігурації за промовчанням це означає, що цифри з плаваючою точкою тепер друкуються з повною точністю цими функціями налагодження.
    
-   Якщо масив, що повертається [\_\_sleep()](language.oop5.magic.html#object.sleep), Містить неіснуючі властивості, тепер вони автоматично проігноруються. Раніше такі властивості були б серіалізовані, якби вони мали значення **`null`**
    
-   Локаль за замовчуванням під час запуску тепер завжди буде визначено як `"C"`. За замовчуванням локалі не успадковуються з оточення. Раніше для **`LC_ALL`** було встановлено значення `"C"`, в той час як **`LC_CTYPE`** успадковувався від оточення. Однак деякі функції не враховували успадковану локаль без явного виклику [setlocale()](function.setlocale.html). Явний виклик [setlocale()](function.setlocale.html) тепер потрібно завжди, якщо компонент локалі повинен бути змінений зі значенням за замовчуванням.
    
-   Застарілий резервний варіант DES в [crypt()](function.crypt.html) був видалений. Якщо в [crypt()](function.crypt.html) передається невідомий формат солі, функція завершиться помилкою з `*0` замість повернення до слабкого хешу DES.
    
-   При вказанні значень поза допустимим діапазоном для SHA256/SHA512 [crypt()](function.crypt.html) тепер буде видана помилка `*0` замість обмеження до найближчої межі. Це відповідає поведінці glibc.
    
-   Результат функцій сортування міг змінитися, якщо масиві є однакові елементи.
    
-   Будь-які функції, що приймають callback-функції, які явно не вказані для прийому параметрів посилання, тепер будуть попереджати, якщо використовується callback-функція з посиланнями. Наприклад, [array\_filter()](function.array-filter.html) і [array\_reduce()](function.array-reduce.html). Раніше так було більшість функцій, але не всі.
    
-   Обгортка HTTP-потоку, використовувана такими функціями, як [file\_get\_contents()](function.file-get-contents.html), тепер за промовчанням оголошує HTTP/1.1, а не HTTP/1.0. Не змінює поведінки клієнта, але може змусити сервери реагувати інакше. Щоб зберегти стару поведінку, установіть параметр контексту потоку `'protocol_version'`, наприклад:
    
    ```php
    <?php
    $ctx = stream_context_create(['http' => ['protocol_version' => '1.0']]);
    echo file_get_contents('http://example.org', false, $ctx);
    ?>
    ```
    
-   Виклик [crypt()](function.crypt.html) без явної передачі солі більше не підтримується. Якщо ви хочете створити надійний хеш із автоматично згенерованою сіллю, використовуйте натомість [password\_hash()](function.password-hash.html)
    
-   [substr()](function.substr.html) [mb\_substr()](function.mb-substr.html) [iconv\_substr()](function.iconv-substr.html) і [grapheme\_substr()](function.grapheme-substr.html) тепер послідовно фіксують зміщення межі кордону рядка. Раніше, у деяких випадках, замість порожнього рядка повертався **`false`**
    
-   У Windows функції виконання програм ([proc\_open()](function.proc-open.html) [exec()](function.exec.html) [popen()](function.popen.html) і т.д.) з використанням оболонки тепер послідовно виконують **%comspec% /s /c "$commandline"**яка робить те ж саме, що і виконання **$commandline** (без додаткових лапок).
    

### Зовсім

-   Параметр `auto_release` в [sem\_get()](function.sem-get.html) був змінений, щоб набувати логічних значень (bool), а не цілі числа (int).

### Tidy

-   Параметр `use_include_path`, який не використовувався внутрішньо, був видалений з [tidy\_repair\_string()](tidy.repairstring.html)
    
-   [tidy::repairString()](tidy.repairstring.html) і [tidy::repairFile()](tidy.repairfile.html) стали статичними методами
    

### PHP-лексер (Tokenizer)

-   У лексемах `T_COMMENT` більше не буде символу нового рядка наприкінці. Натомість новий рядок буде частиною наступної лексеми `T_WHITESPACE`. Слід зазначити, що за `T_COMMENT` не завжди слідує пробіл, за ним також може бути `T_CLOSE_TAG` або кінець файлу.
    
-   Імена у просторах імен тепер представлені за допомогою `T_NAME_QUALIFIED` `Foo\Bar` `T_NAME_FULLY_QUALIFIED` `\Foo\Bar`) та лексеми `T_NAME_RELATIVE` `namespace\Foo\Bar` . `T_NS_SEPARATOR` використовується тільки для автономних розділювачів простору імен і лише синтаксично дійсний у поєднанні з оголошеннями групового використання.
    

### XMLReader

[XMLReader::open()](xmlreader.open.html) і [XMLReader::xml()](xmlreader.xml.html) тепер є статичними методами. Їх, як і раніше, можна викликати як методи екземпляра, але наступні класи повинні оголошувати їх як статичні, якщо вони перевизначають ці методи.

### XML-RPC

Модуль XML-RPC був переміщений до PECL і не є частиною дистрибутива PHP.

### Zip

**`ZipArchive::OPSYS_Z_CPM`** була видалена (у цьому імені була помилка). Використовуйте замість неї **`ZipArchive::OPSYS_CPM`**

### Zlib

-   [gzgetss()](function.gzgetss.html) видалено.
    
-   [zlib.output\_compression](zlib.configuration.html#ini.zlib.output-compression) більше не вимикається автоматично для `Content-Type: image/*`
    

### Пакети тестів PHP для Windows

Скрипт виконання тестів був перейменований з run-test.php на run-tests.php, щоб відповідати його імені в php-src.
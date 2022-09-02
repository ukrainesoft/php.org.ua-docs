---
navigation:
  - migration80.new-features.md: « Новая функциональность
  - migration80.deprecated.md: 'Функціональність, оголошена застарілою в PHP 8.0.x'
  - index.md: PHP Manual
  - migration80.md: Миграция с PHP 7.4.x на PHP 8.0.x
title: 'Зміни, що ламають зворотну сумісність'
---
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
    
-   Методи з тим самим ім'ям, як і клас, більше не інтерпретуються як конструктори. Натомість слід використовувати метод [construct()](language.oop5.decon.md#object.construct)
    
-   Можливість статичного виклику нестатичних методів видалено. Таким чином, [ісcallable()](function.is-callable.md) завершиться помилкою під час перевірки нестатичного методу з ім'ям класу (необхідно перевіряти з екземпляром об'єкта).
    
-   Приведення типів `(real)` і `(unset)` видалено.
    
-   INI-директива [trackerrors](errorfunc.configuration.md#ini.track-errors) видалено. Це означає, що phperrormsg більше не є актуальним. Замість нього можна використовувати функцію [errorgetlast()](function.error-get-last.md)
    
-   Можливість визначати константи без урахування регістру було видалено. Третій аргумент [define()](function.define.md) більше не може бути **`true`**
    
-   Можливість вказувати автозавантажувач за допомогою функції [autoload()](function.autoload.md) було видалено. Натомість слід використовувати [splautoloadregister()](function.spl-autoload-register.md)
    
-   Аргумент `errcontext` більше не передається в користувальницькі обробники помилок, заданих за допомогою [seterrorhandler()](function.set-error-handler.md)
    
-   [createfunction()](function.create-function.md) було видалено. Замість неї можна використовувати анонімні функції.
    
-   [each()](function.each.md) було видалено. Замість неї можна використовувати [foreach](control-structures.foreach.md) або [ArrayIterator](class.arrayiterator.md)
    
-   Можливість відв'язати це від замикань, які були створені з методу з використанням [Closure::fromCallable()](closure.fromcallable.md) або [ReflectionMethod::getClosure()](reflectionmethod.getclosure.md), було видалено.
    
-   Можливість відв'язати це від належних замикань, що містять використання цього, також була видалена.
    
-   Можливість використання [arraykeyexists()](function.array-key-exists.md) з об'єктами було видалено. Натомість можна використовувати [isset()](function.isset.md) або [propertyexists()](function.property-exists.md)
    
-   Робота параметра `key` у функції [arraykeyexists()](function.array-key-exists.md) тепер наведена відповідно до [isset()](function.isset.md) та звичайним доступом до масиву. Всі типи ключів тепер використовують звичайне приведення типів, масив/об'єкт до ключа призведе до викидання [TypeError](class.typeerror.md)
    
-   Будь-який масив, у якого в якості першого числового ключа вказано число n, використовуватиме n+1 для свого наступного неявного ключа, навіть якщо n негативно.
    
-   Рівень errorreporting за замовчуванням тепер **`E_ALL`**. Раніше він виключав **`E_NOTICE`** і **`E_DEPRECATED`**
    
-   [displaystartuperrors](errorfunc.configuration.md#ini.display-startup-errors) тепер включено за замовчуванням.
    
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
    
-   Ряд попереджень перетворено на винятки [Error](class.error.md)
    
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
    
-   Несподівані символи у вихідних файлах (наприклад, байти NUL за межами рядків) тепер призводять до виключення [ParseError](class.parseerror.md) замість попередження під час компіляції.
    
-   Неперехоплені винятки тепер проходять процедуру "чистого завершення", це означає, що після неперехопленого виключення викликатимуться деструктори.
    
-   Фатальна помилка часу компіляції "Only variables can be passed by reference" була відкладена до часу виконання та перетворена на виключення [Error](class.error.md) "Argument cannot be passed by reference".
    
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
    
-   Арифметичні та побітові оператори `+` `-` `*` `/` `**` `%` `<<` `>>` `&` `|` `^` `~` `++` `--` тепер будуть послідовно видавати [TypeError](class.typeerror.md), коли одним з операндів є масив (array), ресурс ([resource](language.types.resource.md)) чи не перевантажений об'єкт (object). Єдиним винятком із цього правила є операція злиття масивів `+`яка, як і раніше, підтримується.
    
-   Приведення з плаваючою точкою в рядок тепер завжди поводитиметься незалежно від локалі.
    
    ```php
    <?php
    setlocale(LC_ALL, "de_DE");
    // Ранее:  3,14
    // Теперь: 3.14
    ?>
    ```
    
    Дивіться [printf()](function.printf.md) [numberformat()](function.number-format.md) і **NumberFormatter()** для отримання інформації про способи настроювання форматування чисел.
    
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
    
-   Якщо у конструкторі об'єкта використовується [exit()](function.exit.md), Деструктор об'єкта більше не буде викликатися. Це відповідає поведінці, коли конструктор викидає виняток.
    
-   Імена у просторі імен більше не можуть містити прогалини: `Foo\Bar` буде розпізнаватись як ім'я в просторі імен, `Foo \ Bar` - Ні. І навпаки, зарезервовані ключові слова тепер дозволені як сегменти простору імен, що також може змінити інтерпретацію коду: `new\x` тепер збігається з `constant('new\x')`, але не з `new \x()`
    
-   Для вкладених тернарних операторів тепер потрібна явна вказівка ​​дужок.
    
-   [debugbacktrace()](function.debug-backtrace.md) і [Exception::getTrace()](exception.gettrace.md) більше не надаватимуть посилання на аргументи. Неможливо змінити аргументи функції через трасування.
    
-   Обробка числових рядків була змінена, щоб зробити її більш зрозумілою і менш схильною до помилок. Завершальні прогалини тепер дозволено у числових рядках для узгодженості з тим, як обробляються початкові прогалини. В основному це впливає на:
    
    -   функцію [ісnumeric()](function.is-numeric.md)
    -   Порівняння рядків з рядками
    -   Оголошення типів
    -   Операції збільшення та зменшення
    
    Поняття "провідний числовий рядок" в основному було відкинуто; випадки, коли це залишилося, є для полегшення міграції. Рядки, які видавали **`E_NOTICE`** "A non well-formed numeric value encountered", тепер видаватимуть **`E_WARNING`** "A non-numeric value encountered", а всі рядки, які видавали **`E_WARNING`** "A non-numeric value encountered" тепер видаватиме [TypeError](class.typeerror.md). В основному це впливає на:
    
    -   Арифметичні операції
    -   Побітові операції
    
    Ця зміна **`E_WARNING`** на [TypeError](class.typeerror.md) також впливає на **`E_WARNING`** "Illegal string offset 'string'" для неприпустимих зсувів рядка. Поведінка явних наведень до int/float з рядків не змінилася.
    
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
-   Ключі масиву [calluserfuncarray()](function.call-user-func-array.md) тепер інтерпретуватимуться як імена параметрів, а не ігноруватимуться.
    
-   Оголошення функції з ім'ям `assert()` всередині простору імен більше не допускається та викликає **`E_COMPILE_ERROR`**. Функція [assert()](function.assert.md) піддається спеціальної обробки з боку движка, що може призвести до неузгодженої поведінки щодо однойменної функції у просторі імен.
    

### Перетворення ресурсів на об'єкти

Декілька ресурсів ([resource](language.types.resource.md)) були перетворені на об'єкти (object). Перевірки значення, що повертається з використанням [ісresource()](function.is-resource.md) слід замінити перевірками на **`false`**

-   [curlinit()](function.curl-init.md) тепер повертає об'єкт [CurlHandle](class.curlhandle.md) замість ресурсу ([resource](language.types.resource.md)). Функція [curlclose()](function.curl-close.md) більше не має сенсу, натомість екземпляр [CurlHandle](class.curlhandle.md) автоматично знищується, якщо на нього немає посилання.
    
-   [curlmultiinit()](function.curl-multi-init.md) тепер повертає об'єкт [CurlMultiHandle](class.curlmultihandle.md) замість ресурсу ([resource](language.types.resource.md)). Функція [curlmulticlose()](function.curl-multi-close.md) більше не має сенсу, натомість екземпляр [CurlMultiHandle](class.curlmultihandle.md) автоматично знищується, якщо на нього немає посилання.
    
-   [curlshareinit()](function.curl-share-init.md) тепер повертає об'єкт [CurlShareHandle](class.curlsharehandle.md) замість ресурсу ([resource](language.types.resource.md)). Функція [curlshareclose()](function.curl-share-close.md) більше не має сенсу, натомість екземпляр [CurlShareHandle](class.curlsharehandle.md) автоматично знищується, якщо на нього немає посилання.
    
-   [enchantbrokerinit()](function.enchant-broker-init.md) тепер повертає об'єкт [EnchantBroker](class.enchantbroker.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [enchantbrokerrequestdict()](function.enchant-broker-request-dict.md) і [enchantbrokerrequestpwldict()](function.enchant-broker-request-pwl-dict.md) тепер повертають [EnchantDictionary](class.enchantdictionary.md) об'єкт замість ресурсу ([resource](language.types.resource.md)
    
-   Модуль GD тепер використовує об'єкти [GdImage](class.gdimage.md) як базова структура даних для зображень, а не ресурси ([resource](language.types.resource.md)). Функція [imagedestroy()](function.imagedestroy.md) більше немає сенсу; натомість екземпляр [GdImage](class.gdimage.md) автоматично знищується, якщо на нього немає посилання.
    
-   [opensslx509read()](function.openssl-x509-read.md) і [opensslcsrsign()](function.openssl-csr-sign.md) тепер повертають об'єкт [OpenSSLCertificate](class.opensslcertificate.md) замість ресурсу ([resource](language.types.resource.md)). Функція [opensslx509free()](function.openssl-x509-free.md) оголошена застарілою і більше не має сенсу, натомість екземпляр [OpenSSLCertificate](class.opensslcertificate.md) автоматично знищується, якщо на нього більше не посилаються.
    
-   [opensslcsrnew()](function.openssl-csr-new.md) тепер повертає об'єкт [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [opensslpkeynew()](function.openssl-pkey-new.md) тепер повертає об'єкт [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) замість ресурсу ([resource](language.types.resource.md)). Функція [opensslpkeyfree()](function.openssl-pkey-free.md) оголошена застарілою і більше не має сенсу, натомість екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) автоматично знищується, якщо на нього більше не посилаються.
    
-   [shmopopen()](function.shmop-open.md) тепер повертає об'єкт [Shmop](class.shmop.md) замість ресурсу ([resource](language.types.resource.md)). Функція [shmopclose()](function.shmop-close.md) більше немає сенсу і оголошена застарілою; натомість екземпляр [Shmop](class.shmop.md) автоматично знищується, якщо на нього більше не посилаються.
    
-   [socketcreate()](function.socket-create.md) [socketcreatelisten()](function.socket-create-listen.md) [socketaccept()](function.socket-accept.md) [socketimportstream()](function.socket-import-stream.md) [socketaddrinfoconnect()](function.socket-addrinfo-connect.md) [socketaddrinfobind()](function.socket-addrinfo-bind.md) і [socketwsaprotocolinfoimport()](function.socket-wsaprotocol-info-import.md) тепер повертають об'єкт [Socket](class.socket.md) замість ресурсу ([resource](language.types.resource.md) . [socketaddrinfolookup()](function.socket-addrinfo-lookup.md) тепер повертає масив об'єктів [AddressInfo](class.addressinfo.md) замість масиву ресурсів ([resource](language.types.resource.md)
    
-   [msggetqueue()](function.msg-get-queue.md) тепер повертають об'єкт [SysvMessageQueue](class.sysvmessagequeue.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [semget()](function.sem-get.md) тепер повертають об'єкт [SysvSemaphore](class.sysvsemaphore.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [shmattach()](function.shm-attach.md) тепер повертають об'єкт [SysvSharedMemory](class.sysvsharedmemory.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [xmlparsercreate()](function.xml-parser-create.md) і [xmlparsercreatens()](function.xml-parser-create-ns.md) тепер повертають об'єкт [XMLParser](class.xmlparser.md) замість ресурсу ([resource](language.types.resource.md)). Функція [xmlparserfree()](function.xml-parser-free.md) більше не має сенсу, натомість екземпляр XMLParser автоматично знищується, якщо на нього більше не посилаються.
    
-   Функції [XMLWriter](book.xmlwriter.md) тепер приймають та повертають, відповідно, об'єкти [XMLWriter](class.xmlwriter.md) замість ресурсів ([resource](language.types.resource.md)
    
-   [inflateinit()](function.inflate-init.md) тепер повертає об'єкт [InflateContext](class.inflatecontext.md) замість ресурсу ([resource](language.types.resource.md)
    
-   [deflateinit()](function.deflate-init.md) тепер повертає об'єкт [DeflateContext](class.deflatecontext.md) замість ресурсу ([resource](language.types.resource.md)
    

### COM та .Net (Windows)

Можливість імпорту констант без урахування регістру з бібліотек типів було видалено. Другий аргумент [comloadtypelib()](function.com-load-typelib.md) більше не може бути false; [com.autoregistercasesensitive](com.configuration.md#ini.com.autoregister-casesensitive) більше не можна вимкнути; Маркери без урахування регістру в [com.typelibfile](com.configuration.md#ini.com.typelib-file) ігноруються.

### CURL

**`CURLOPT_POSTFIELDS`** більше не сприймає об'єкти як масиви. Щоб інтерпретувати об'єкт як масив, виконайте явне приведення `(array)`. Те саме стосується й інших параметрів, що приймають масиви.

### дата і час

Для роботи функцій [mktime()](function.mktime.md) і [gmmktime()](function.gmmktime.md) тепер потрібно хоча б один аргумент . [time()](function.time.md) може використовуватись для отримання поточної позначки часу.

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

-   [enchantbrokerlistdicts()](function.enchant-broker-list-dicts.md) [enchantbrokerdescribe()](function.enchant-broker-describe.md) і [enchantdictsuggest()](function.enchant-dict-suggest.md) тепер повертають порожній масив замість **`null`**

### Exif

[readexifdata()](function.read-exif-data.md) була видалена; Замість неї слід використовувати [exifreaddata()](function.exif-read-data.md)

### Фільтрування даних

-   Прапори **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** для фільтра **`FILTER_VALIDATE_URL`** були видалені . `scheme` і `host` необхідні (і завжди були).
    
-   Типи **`INPUT_REQUEST`** і **`INPUT_SESSION`** для [filterinput()](function.filter-input.md) та її похідних були видалені. Вони ніколи не були реалізовані, а спроба їх використання завжди викликала попередження.
    

### ДД

-   Застарілі функції [image2wbmp()](function.image2wbmp.md) були вилучені.
    
-   Застарілі функції [png2wbmp()](function.png2wbmp.md) і [jpeg2wbmp()](function.jpeg2wbmp.md) були вилучені.
    
-   Параметр `mode` за замовчуванням для функції [imagecropauto()](function.imagecropauto.md) більше не набуває значення `-1`. Натомість слід використовувати **`IMG_CROP_DEFAULT`**
    
-   У Windows, phpgd2.dll перейменований на phpgd.dll
    

### GMP

[gmprandom()](function.gmp-random.md) було видалено. Замість неї слід використовувати [gmprandomrange()](function.gmp-random-range.md) або [gmprandombits()](function.gmp-random-bits.md)

### Iconv

Реалізації iconv, які неправильно встановлюють errno у разі виникнення помилок, більше не підтримуються.

### IMAP

-   Невикористовуваний аргумент `default_host` функції [imapheaderinfo()](function.imap-headerinfo.md) був видалений.
    
-   Функція [imapheader()](function.imap-header.md)яка є псевдонімом [imapheaderinfo()](function.imap-headerinfo.md), було видалено.
    

### Функції інтернаціоналізації

-   Застаріла константа **`INTL_IDNA_VARIANT_2003`** видалено.
    
-   Застаріла константа **`Normalizer::NONE`** видалено.
    

### LDAP

-   Застарілі функції [ldapsort()](function.ldap-sort.md) [ldapcontrolpagedresult()](function.ldap-control-paged-result.md) і [ldapcontrolpagedresultresponse()](function.ldap-control-paged-result-response.md) видалено.
    
-   Змінився інтерфейс [ldapsetrebindproc()](function.ldap-set-rebind-proc.md); параметр `callback` більше не приймає порожні рядки; натомість слід вказувати **`null`**
    

### MBString

-   Директива [mbstring.funcoverload](mbstring.configuration.md#ini.mbstring.func-overload) було видалено. Пов'язані константи **`MB_OVERLOAD_MAIL`** **`MB_OVERLOAD_STRING`** і **`MB_OVERLOAD_REGEX`** також було видалено. Зрештою, записи `"func_overload"` і `"func_overload_list"` в [мбgetinfo()](function.mb-get-info.md) були вилучені.
    
-   [мбparsestr()](function.mb-parse-str.md) більше не можна використовувати без передачі масиву результатів.
    
-   Видалено низку застарілих псевдонімів mbregex. У наступному списку вказано, які функції слід використовувати замість них:
    
    -   **mbregexencoding()** [мбregexencoding()](function.mb-regex-encoding.md)
    -   **mbereg()** [мбereg()](function.mb-ereg.md)
    -   **mberegi()** [мбeregi()](function.mb-eregi.md)
    -   **mberegreplace()** [мбeregreplace()](function.mb-ereg-replace.md)
    -   **mberegireplace()** [мбeregireplace()](function.mb-eregi-replace.md)
    -   **mbsplit()** [мбsplit()](function.mb-split.md)
    -   **mberegmatch()** [мбeregmatch()](function.mb-ereg-match.md)
    -   **mberegsearch()** [мбeregsearch()](function.mb-ereg-search.md)
    -   **mberegsearchpos()** [мбeregsearchpos()](function.mb-ereg-search-pos.md)
    -   **mberegsearchregs()** [мбeregsearchregs()](function.mb-ereg-search-regs.md)
    -   **mberegsearchinit()** [мбeregsearchinit()](function.mb-ereg-search-init.md)
    -   **mberegsearchgetregs()** [мбeregsearchgetregs()](function.mb-ereg-search-getregs.md)
    -   **mberegsearchgetpos()** [мбeregsearchgetpos()](function.mb-ereg-search-getpos.md)
    -   **mberegsearchsetpos()** [мбeregsearchsetpos()](function.mb-ereg-search-setpos.md)
-   Модифікатор `e` для [мбeregreplace()](function.mb-ereg-replace.md) був видалений. Замість нього слід використовувати[мбeregreplacecallback()](function.mb-ereg-replace-callback.md)
    
-   Аргумент нерядкового шаблону для [мбeregreplace()](function.mb-ereg-replace.md) тепер інтерпретуватиметься як рядок замість кодової точки ASCII. Попередню поведінку можна відновити явним викликом [chr()](function.chr.md)
    
-   Аргумент `needle` для функцій [мбstrpos()](function.mb-strpos.md) [мбstrrpos()](function.mb-strrpos.md) [мбstripos()](function.mb-stripos.md) [мбstrripos()](function.mb-strripos.md) [мбstrstr()](function.mb-strstr.md) [мбstristr()](function.mb-stristr.md) [мбstrrchr()](function.mb-strrchr.md) і [мбstrrichr()](function.mb-strrichr.md) тепер може бути порожнім.
    
-   Параметр `is_hex`, який не використовувався для внутрішніх цілей, був видалений з [мбdecodenumericentity()](function.mb-decode-numericentity.md)
    
-   Застаріла поведінка передачі кодування як третій аргумент замість зміщення функції [мбstrrpos()](function.mb-strrpos.md) було видалено; замість цього як четвертий аргумент слід вказати явне зміщення `0` з кодуванням.
    
-   Псевдоніми кодування символів `ISO_8859-*` були замінені на псевдоніми `ISO8859-*` для кращої сумісності із модулем iconv. Псевдоніми mbregex ISO 8859 з підкресленням (`ISO_8859_*` і `ISO8859_*`) також були видалені.
    
-   [мбereg()](function.mb-ereg.md) і [мбeregi()](function.mb-eregi.md) тепер повертатимуть логічне значення **`true`**, у разі знайденого збігу. Раніше вони повертали ціле число `1`, якщо аргумент `matches` не було передано, або `max(1, strlen($matches[0]))`, якщо `matches` був не пустий.
    

### OCI8

-   Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.md), а клас **OCI-Collection** - у [OCICollection](class.ocicollection.md) для імені сумісність забезпечується засобами інструкції типу arginfo PHP 8.
    
-   Деякі функції псевдонімів оголошено застарілим.
    
-   [ociinternaldebug()](function.oci-internal-debug.md) та її псевдонім [ociinternaldebug()](function.ociinternaldebug.md) були вилучені.
    

### ODBC

-   [odbcconnect()](function.odbc-connect.md) більше не використовує з'єднання повторно.
    
-   Параметр, що не використовується `flags` функції [odbcexec()](function.odbc-exec.md) був видалений.
    

### OpenSSL

-   [opensslseal()](function.openssl-seal.md) і [opensslopen()](function.openssl-open.md) тепер вимагають передачі `method`, так як попереднє значення за замовчуванням `"RC4"` вважається небезпечним.

### Регулярні вирази (сумісні з Perl)

При передачі неприпустимих послідовностей, що управляють, вони більше не інтерпретуються як літерали. Така поведінка раніше вимагала модифікатора `X`, що тепер ігнорується.

### Об'єкти даних PHP

-   Режим обробки помилок за умовчанням було змінено з "тихого" (silent) на "виключення" (exceptions). Детальніше дивіться [Ошибки и обработка ошибок](pdo.error-handling.md)
    
-   Змінилися сигнатури деяких методів PDO:
    
    -   `PDO::query(string $query, ?int $fetchMode = null, mixed ...$fetchModeArgs)`
    -   `PDOStatement::setFetchMode(int $mode, mixed ...$args)`

### PDO ODBC

Директива php.ini [pdoodbc.db2instancename](ref.pdo-odbc.md#ini.pdo-odbc.db2-instance-name) було видалено.

### PDO MySQL

[PDO::inTransaction()](pdo.intransaction.md) тепер повідомляє фактичний стан транзакції підключення, а не про приблизний від PDO. Якщо запит, за умови "неявної фіксації", виконується, то [PDO::inTransaction()](pdo.intransaction.md) згодом поверне **`false`**, оскільки транзакція буде неактивною.

### PostgreSQL

-   Застарілий синтаксис [пгconnect()](function.pg-connect.md) за допомогою кількох параметрів замість рядка підключення більше не підтримується.
    
-   Застарілі сигнатури [пглоimport()](function.pg-lo-import.md) і [пглоexport()](function.pg-lo-export.md), що передають з'єднання як останній аргумент, більше не підтримуються. Натомість з'єднання має бути передано першим аргументом.
    
-   [пгfetchall()](function.pg-fetch-all.md) тепер повертатиме порожній масив замість **`false`** для наборів результатів із відсутніми рядками.
    

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
-   Метод [ReflectionType::toString()](reflectiontype.tostring.md) тепер повертатиме повне налагоджувальне уявлення типу і більше не є застарілим. Зокрема, результат включатиме індикатор допустимості значень NULL для типів, що допускають значення NULL. Формат значення, що повертається, нестабільний і може змінюватися в залежності від версії PHP.
    
-   Методи Reflection export() були видалені. Натомість об'єкти reflection можуть бути перетворені на рядок.
    
-   [ReflectionMethod::isConstructor()](reflectionmethod.isconstructor.md) і [ReflectionMethod::isDestructor()](reflectionmethod.isdestructor.md) тепер також повертають **`true`** для методів інтерфейсів [construct()](language.oop5.decon.md#object.construct) і [destruct()](language.oop5.decon.md#object.destruct). Раніше це було вірно лише для методів класів та трейтів.
    
-   Метод **ReflectionType::isBuiltin()** переміщений у [ReflectionNamedType](class.reflectionnamedtype.md). У [ReflectionUnionType](class.reflectionuniontype.md) цього методу немає.
    

### Сокети

-   Застарілі `flags` **`AI_IDN_ALLOW_UNASSIGNED`** і **`AI_IDN_USE_STD3_ASCII_RULES`** для [socketaddrinfolookup()](function.socket-addrinfo-lookup.md) були вилучені.

### Стандартна бібліотека PHP (SPL)

-   [SplFileObject::fgetss()](splfileobject.fgetss.md) був видалений.
    
-   [SplFileObject::seek()](splfileobject.seek.md) тепер завжди переміщається початку рядка. Раніше, позиція `>=1` переміщала на початок наступні рядки.
    
-   [SplHeap::compare()](splheap.compare.md) тепер вказує сигнатуру методу. Наслідуючі класи, які реалізують цей метод, тепер повинні використовувати сумісну сигнатуру методу.
    
-   [SplDoublyLinkedList::push()](spldoublylinkedlist.push.md) [SplDoublyLinkedList::unshift()](spldoublylinkedlist.unshift.md) і [SplQueue::enqueue()](splqueue.enqueue.md) тепер повертають void замість **`true`**
    
-   [splautoloadregister()](function.spl-autoload-register.md) тепер завжди викидатиме [TypeError](class.typeerror.md) для неприпустимих аргументів, тому другий аргумент `do_throw` ігнорується, якщо для нього встановлено значення **`false`**
    
-   [SplFixedArray](class.splfixedarray.md) тепер є [IteratorAggregate](class.iteratoraggregate.md), а не [Iterator](class.iterator.md). . [SplFixedArray::rewind()](splfixedarray.rewind.md) [SplFixedArray::current()](splfixedarray.current.md) [SplFixedArray::key()](splfixedarray.key.md) [SplFixedArray::next()](splfixedarray.next.md) і [SplFixedArray::valid()](splfixedarray.valid.md) були вилучені. Замість них було додано **SplFixedArray::getIterator()**. Будь-який код, який використовує явну ітерацію над SplFixedArray, тепер має отримати [Iterator](class.iterator.md) за допомогою **SplFixedArray::getIterator()**. Це означає, що [SplFixedArray](class.splfixedarray.md) тепер безпечно використовувати у вкладених циклах.
    

### Бібліотека стандартних функцій

-   [assert()](function.assert.md) більше не виконуватиме рядкові аргументи, натомість вони будуть оброблятися як будь-які звичайні аргументи. Таким чином, замість `assert('$a == $b')` слід використовувати `assert($a == $b)`. INI-директива [assert.quieteval](info.configuration.md#ini.assert.quiet-eval) та константа **`ASSERT_QUIET_EVAL`** були видалені, оскільки вони не мають сенсу.
    
-   [parsestr()](function.parse-str.md) більше не можна використовувати без зазначення масиву результатів.
    
-   Фільтр [string.striptags](filters.string.md#filters.string.strip_tags) видалено.
    
-   Аргумент `needle` функцій [strpos()](function.strpos.md) [strrpos()](function.strrpos.md) [stripos()](function.stripos.md) [strripos()](function.strripos.md) [strstr()](function.strstr.md) [strchr()](function.strchr.md) [strrchr()](function.strrchr.md) і [stristr()](function.stristr.md) тепер завжди інтерпретуватиметься як рядок. Раніше невеликі потреби інтерпретувалися як кодова точка ASCII. Явний виклик [chr()](function.chr.md) може використовуватись для відновлення попередньої поведінки.
    
-   Аргумент `needle` функцій [strpos()](function.strpos.md) [strrpos()](function.strrpos.md) [stripos()](function.stripos.md) [strripos()](function.strripos.md) [strstr()](function.strstr.md) [stristr()](function.stristr.md) і [strrchr()](function.strrchr.md) тепер може бути порожнім.
    
-   Аргумент `length` функцій [substr()](function.substr.md) [substrcount()](function.substr-count.md) [substrcompare()](function.substr-compare.md) і [iconvsubstr()](function.iconv-substr.md) тепер може бути **`null`**. Значення **`null`** означає відсутність аргументу довжини, і тому функції повернуть залишок рядка замість порожнього рядка.
    
-   Аргумент `length` функції [arraysplice()](function.array-splice.md) тепер може бути **`null`**. Передача значення **`null`** означає відсутність аргументу, тому функція видалити все, починаючи від `offset` до кінця масиву.
    
-   Аргумент `args` функцій [vsprintf()](function.vsprintf.md) [vfprintf()](function.vfprintf.md) і [vprintf()](function.vprintf.md) тепер має бути масивом. Раніше приймався будь-який тип.
    
-   Параметр `'salt'` функції [passwordhash()](function.password-hash.md) більше не підтримується. Якщо використовується опція `'salt'`, генерується попередження, передана сіль ігнорується, а замість неї використовується сгенерована сіль.
    
-   Функція [quotemeta()](function.quotemeta.md) тепер повертатиме порожній рядок, якщо було передано порожній рядок. Раніше поверталося **`false`**
    
-   Видалено такі функції:
    
    -   [hebrevc()](function.hebrevc.md)
    -   [convertcyrstring()](function.convert-cyr-string.md)
    -   [moneyformat()](function.money-format.md)
    -   [ezmlmhash()](function.ezmlm-hash.md)
    -   [restoreincludepath()](function.restore-include-path.md)
    -   [getmagicquotesgpc()](function.get-magic-quotes-gpc.md)
    -   [getmagicquotesruntime()](function.get-magic-quotes-runtime.md)
    -   [fgetss()](function.fgetss.md)
-   **`FILTER_SANITIZE_MAGIC_QUOTES`** видалено.
    
-   Виклик [implode()](function.implode.md) з параметрами у зворотному порядку `($pieces, $glue)` більше не підтримується.
    
-   [parseurl()](function.parse-url.md) тепер буде розрізняти відсутні та порожні запити та фрагменти:
    
    -   `http://example.com/foo → query = null, fragment = null`
    -   `http://example.com/foo? → query = "", fragment = null`
    -   `http://example.com/foo# → query = null, fragment = ""`
    -   `http://example.com/foo?# → query = "", fragment = ""`
    
    Раніше у всіх випадках query та fragment були **`null`**
    
-   [vardump()](function.var-dump.md) і [debugzvaldump()](function.debug-zval-dump.md) тепер друкуватимуть числа з плаваючою точкою, використовуючи [serializeprecision](ini.core.md#ini.serialize-precision), а не [precision](ini.core.md#ini.precision). У конфігурації за промовчанням це означає, що цифри з плаваючою точкою тепер друкуються з повною точністю цими функціями налагодження.
    
-   Якщо масив, що повертається [sleep()](language.oop5.magic.md#object.sleep), Містить неіснуючі властивості, тепер вони автоматично проігноруються. Раніше такі властивості були б серіалізовані, якби вони мали значення **`null`**
    
-   Локаль за замовчуванням під час запуску тепер завжди буде визначено як `"C"`. За замовчуванням локалі не успадковуються з оточення. Раніше для **`LC_ALL`** було встановлено значення `"C"`, в той час як **`LC_CTYPE`** успадковувався від оточення. Однак деякі функції не враховували успадковану локаль без явного виклику [setlocale()](function.setlocale.md). Явний виклик [setlocale()](function.setlocale.md) тепер потрібно завжди, якщо компонент локалі повинен бути змінений зі значенням за замовчуванням.
    
-   Застарілий резервний варіант DES в [crypt()](function.crypt.md) був видалений. Якщо в [crypt()](function.crypt.md) передається невідомий формат солі, функція завершиться помилкою з `*0` замість повернення до слабкого хешу DES.
    
-   При вказанні значень поза допустимим діапазоном для SHA256/SHA512 [crypt()](function.crypt.md) тепер буде видана помилка `*0` замість обмеження до найближчої межі. Це відповідає поведінці glibc.
    
-   Результат функцій сортування міг змінитися, якщо масиві є однакові елементи.
    
-   Будь-які функції, що приймають callback-функції, які явно не вказані для прийому параметрів посилання, тепер будуть попереджати, якщо використовується callback-функція з посиланнями. Наприклад, [arrayfilter()](function.array-filter.md) і [arrayreduce()](function.array-reduce.md). Раніше так було більшість функцій, але не всі.
    
-   Обгортка HTTP-потоку, використовувана такими функціями, як [filegetcontents()](function.file-get-contents.md), тепер за промовчанням оголошує HTTP/1.1, а не HTTP/1.0. Не змінює поведінки клієнта, але може змусити сервери реагувати інакше. Щоб зберегти стару поведінку, установіть параметр контексту потоку `'protocol_version'`, наприклад:
    
    ```php
    <?php
    $ctx = stream_context_create(['http' => ['protocol_version' => '1.0']]);
    echo file_get_contents('http://example.org', false, $ctx);
    ?>
    ```
    
-   Виклик [crypt()](function.crypt.md) без явної передачі солі більше не підтримується. Якщо ви хочете створити надійний хеш із автоматично згенерованою сіллю, використовуйте натомість [passwordhash()](function.password-hash.md)
    
-   [substr()](function.substr.md) [мбsubstr()](function.mb-substr.md) [iconvsubstr()](function.iconv-substr.md) і [graphemesubstr()](function.grapheme-substr.md) тепер послідовно фіксують зміщення межі кордону рядка. Раніше, у деяких випадках, замість порожнього рядка повертався **`false`**
    
-   У Windows функції виконання програм ([procopen()](function.proc-open.md) [exec()](function.exec.md) [popen()](function.popen.md) і т.д.) з використанням оболонки тепер послідовно виконують \*\*%comspec% /s /c "$commandline"\*\*яка робить те ж саме, що і виконання **$commandline** (без додаткових лапок).
    

### Зовсім

-   Параметр `auto_release` в [semget()](function.sem-get.md) був змінений, щоб набувати логічних значень (bool), а не цілі числа (int).

### Tidy

-   Параметр `use_include_path`, який не використовувався внутрішньо, був видалений з [tidyrepairstring()](tidy.repairstring.md)
    
-   [tidy::repairString()](tidy.repairstring.md) і [tidy::repairFile()](tidy.repairfile.md) стали статичними методами
    

### PHP-лексер (Tokenizer)

-   У лексемах `T_COMMENT` більше не буде символу нового рядка наприкінці. Натомість новий рядок буде частиною наступної лексеми `T_WHITESPACE`. Слід зазначити, що за `T_COMMENT` не завжди слідує пробіл, за ним також може бути `T_CLOSE_TAG` або кінець файлу.
    
-   Імена у просторах імен тепер представлені за допомогою `T_NAME_QUALIFIED` `Foo\Bar` `T_NAME_FULLY_QUALIFIED` `\Foo\Bar`) та лексеми `T_NAME_RELATIVE` `namespace\Foo\Bar` . `T_NS_SEPARATOR` використовується тільки для автономних розділювачів простору імен і лише синтаксично дійсний у поєднанні з оголошеннями групового використання.
    

### XMLReader

[XMLReader::open()](xmlreader.open.md) і [XMLReader::xml()](xmlreader.xml.md) тепер є статичними методами. Їх, як і раніше, можна викликати як методи екземпляра, але наступні класи повинні оголошувати їх як статичні, якщо вони перевизначають ці методи.

### XML-RPC

Модуль XML-RPC був переміщений до PECL і не є частиною дистрибутива PHP.

### Zip

**`ZipArchive::OPSYS_Z_CPM`** була видалена (у цьому імені була помилка). Використовуйте замість неї **`ZipArchive::OPSYS_CPM`**

### Zlib

-   [gzgetss()](function.gzgetss.md) видалено.
    
-   [zlib.outputcompression](zlib.configuration.md#ini.zlib.output-compression) більше не вимикається автоматично для `Content-Type: image/*`
    

### Пакети тестів PHP для Windows

Скрипт виконання тестів був перейменований з run-test.php на run-tests.php, щоб відповідати його імені в php-src.

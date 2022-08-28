Клас SNMP

-   [« snmpwalkoid](function.snmpwalkoid.html)
    
-   [SNMP::close »](snmp.close.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](book.snmp.html)
    
-   Клас SNMP
    

# Клас SNMP

(PHP 5> = 5.4.0, PHP 7, PHP 8)

## Вступ

Представляє сесію SNMP.

## Огляд класів

```classsynopsis

     
    

    
     
      class SNMP
     
     {

    /* Свойства */
    
     public
     readonly
     array
      $info;

    public
     ?int
      $max_oids;

    public
     int
      $valueretrieval;

    public
     bool
      $quick_print;

    public
     bool
      $enum_print;

    public
     int
      $oid_output_format;

    public
     bool
      $oid_increasing_check;

    public
     int
      $exceptions_enabled;


    /* Методы */
    
   public __construct(    int $version,    string $hostname,    string $community,    int $timeout = -1,    int $retries = -1)

    public close(): bool
public get(array|string $objectId, bool $preserveKeys = false): mixed
public getErrno(): int
public getError(): string
public getnext(array|string $objectId): mixed
public set(array|string $objectId, array|string $type, array|string $value): bool
public setSecurity(    string $securityLevel,    string $authProtocol = "",    string $authPassphrase = "",    string $privacyProtocol = "",    string $privacyPassphrase = "",    string $contextName = "",    string $contextEngineId = ""): bool
public walk(    array|string $objectId,    bool $suffixAsKey = false,    int $maxRepetitions = -1,    int $nonRepeaters = -1): array|false


    /* Константы */
    
     const
     int
      ERRNO_NOERROR = 0;

    const
     int
      ERRNO_GENERIC = 2;

    const
     int
      ERRNO_TIMEOUT = 4;

    const
     int
      ERRNO_ERROR_IN_REPLY = 8;

    const
     int
      ERRNO_OID_NOT_INCREASING = 16;

    const
     int
      ERRNO_OID_PARSING_ERROR = 32;

    const
     int
      ERRNO_MULTIPLE_SET_QUERIES = 64;

    const
     int
      ERRNO_ANY = 126;

    const
     int
      VERSION_1 = 0;

    const
     int
      VERSION_2C = 1;

    const
     int
      VERSION_2c = 1;

    const
     int
      VERSION_3 = 3;

   }
```

## Властивості

maxoids

Максимальний OID для запитів GET/SET/GETBULK

valueretrieval

Контролює спосіб, як повертатимуться значення SNMP

<table class="doctable table"><tbody class="tbody"><tr><td><strong><code>SNMP_VALUE_LIBRARY</code></strong></td><td>Повертані значення будуть такими, ніби повернуто бібліотекою Net-SNMP.</td></tr><tr><td><strong><code>SNMP_VALUE_PLAIN</code></strong></td><td>Повертані значення будуть простими, без інформації про типи SNMP.</td></tr><tr><td><strong><code>SNMP_VALUE_OBJECT</code></strong></td><td>Повертані значення будуть об'єктами з властивостями "value" і "type", де "type" міститиме одну з констант: SNMP_OCTET_STR, SNMP_COUNTER і т.д., а "value" буде залежати від того, чи встановлено <strong><code>SNMP_VALUE_LIBRARY</code></strong> або <strong><code>SNMP_VALUE_PLAIN</code></strong>.</td></tr></tbody></table>

quickprint

Значення `quick_print` у бібліотеці NET-SNMP

Встановлює значення `quick_print` у бібліотеці NET-SNMP. якщо задано як (1), бібліотека SNMP повертатиме значення 'quick printed'. Це означає, що буде надруковано лише значення. Якщо `quick_print` не дозволено (за замовчуванням), бібліотека NET-SNMP друкуватиме додаткову інформацію, включаючи тип значення (тобто IpAddress або OID). Додатково якщо quickprint не дозволено, бібліотека друкуватиме шістнадцяткові значення для всіх рядків коротше чотирьох символів.

enumprint

Контролює спосіб, яким будуть друкуватись значення перерахувань

Параметр перемикає поведінку walk/get і т.д., щоб вони автоматично дивилися значення перерахувань у MIB та повертали їх разом із зрозумілим людині текстом.

oidoutputformat

Контролює формат виводу OID

<table class="doctable table"><caption><strong>OID-подання .1.3.6.1.2.1.1.3.0 для різних значень <var class="varname">oid_output_format</var></strong></caption><tbody class="tbody"><tr><td><strong><code>SNMP_OID_OUTPUT_FULL</code></strong></td><td>.iso.org.dod.internet.mgmt.mib -2.system.sysUpTime.sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_NUMERIC</code></strong></td><td>.1.3.6.1.2.1 .1.3.0</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_MODULE</code></strong></td><td>DISMAN-EVENT-MIB::sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_SUFFIX</code></strong></td><td>sysUpTimeInstance</td></tr><tr><td>&lt; strong&gt;<code>SNMP_OID_OUTPUT_UCD</code></td><td>system.sysUpTime.sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_NONE</code></strong></td><td>Undefined</td></tr></tbody></table>

oidincreasingcheck

Контролює заборону на перевірку збільшення OID під час обходу дерева OID

Деякі агенти SNMP відомі тим, що OID повертають не по порядку, але все одно завершують прохід. Інші агенти, що повертають OID не по порядку і можуть викликати нескінченне зациклювання [SNMP::walk()](snmp.walk.html), поки не буде вичерпано всю пам'ять. Бібліотека PHP SNMP за промовчанням здійснює перевірку збільшення OID і припиняє обхід дерева, якщо визначає можливе кільце, видаючи відповідне попередження. Встановіть oidincreasingcheck у значення **`false`** для заборони перевірки.

exceptionsenabled

Контролює, у яких випадках викидаються винятки SNMPException замість попереджень. Використовуйте побітове АБО з констант **`SNMP::ERRNO_*`**. За промовчанням SNMP не викидає виняток.

info

Властивість доступна тільки для читання, що містить конфігурацію віддаленого агента: ім'я хоста, порт, час за замовчуванням, кількість повторів за замовчуванням

## Обумовлені константи

## Типи помилок SNMP

**`SNMP::ERRNO_NOERROR`**

Помилки SNMP відсутні.

**`SNMP::ERRNO_GENERIC`**

Загальна помилка SNMP.

**`SNMP::ERRNO_TIMEOUT`**

Перевищено час очікування запиту до SNMPагенту.

**`SNMP::ERRNO_ERROR_IN_REPLY`**

SNMPагент повернув помилку у відповідь.

**`SNMP::ERRNO_OID_NOT_INCREASING`**

SNMPагент виявив можливе закольцювання через незбільшення OID під час виконання команд (BULK)WALK. Говорить нам, що віддалений SNMPагент фіктивний.

**`SNMP::ERRNO_OID_PARSING_ERROR`**

Бібліотека не змогла розібрати OID (та/або тип команди SET). Запитів не було.

**`SNMP::ERRNO_MULTIPLE_SET_QUERIES`**

Бібліотека використовує багато запитів для операції SET. Це означає, що операція буде виконуватися без транзакції, і якщо виникне помилка типу або значення, другий або наступні фрагменти можуть завершитися помилкою.

**`SNMP::ERRNO_ANY`**

Усі коди SNMP::ERRNO об'єднані побітовим АБО.

## Версії протоколу SNMP

**`SNMP::VERSION_1`**

**`SNMP::VERSION_2C`** **`SNMP::VERSION_2c`**

**`SNMP::VERSION_3`**

## Зміст

-   [SNMP::close](snmp.close.html) — Закриває сесію SNMP
-   [SNMP::\_\_construct](snmp.construct.html) - Створює екземпляр SNMP, що представляє сесію віддаленого агента SNMP
-   [SNMP::get](snmp.get.html) — Отримує об'єкт SNMP
-   [SNMP::getErrno](snmp.geterrno.html) — Отримує код останньої помилки
-   [SNMP::getError](snmp.geterror.html) — Отримує останнє повідомлення про помилку
-   [SNMP::getnext](snmp.getnext.html) — Отримати об'єкт SNMP, який слідує за цим ідентифікатором об'єкта
-   [SNMP::set](snmp.set.html) — Встановлює значення об'єкта SNMP
-   [SNMP::setSecurity](snmp.setsecurity.html) — Налаштовує пов'язані з безпекою параметри сесії SNMPv3
-   [SNMP::walk](snmp.walk.html) — Отримує піддерево об'єкта SNMP
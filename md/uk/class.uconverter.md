Клас UConverter

-   [« IntlPartsIterator::getBreakIterator](intlpartsiterator.getbreakiterator.html)
    
-   [UConverter::construct »](uconverter.construct.html)
    
-   [PHP Manual](index.html)
    
-   [intl](book.intl.html)
    
-   Клас UConverter
    

# Клас UConverter

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class UConverter
     
     {

    /* Constants */
    
     const
     int
      REASON_UNASSIGNED = 0;

    const
     int
      REASON_ILLEGAL = 1;

    const
     int
      REASON_IRREGULAR = 2;

    const
     int
      REASON_RESET = 3;

    const
     int
      REASON_CLOSE = 4;

    const
     int
      REASON_CLONE = 5;

    const
     int
      UNSUPPORTED_CONVERTER = -1;

    const
     int
      SBCS = 0;

    const
     int
      DBCS = 1;

    const
     int
      MBCS = 2;

    const
     int
      LATIN_1 = 3;

    const
     int
      UTF8 = 4;

    const
     int
      UTF16_BigEndian = 5;

    const
     int
      UTF16_LittleEndian = 6;

    const
     int
      UTF32_BigEndian = 7;

    const
     int
      UTF32_LittleEndian = 8;

    const
     int
      EBCDIC_STATEFUL = 9;

    const
     int
      ISO_2022 = 10;

    const
     int
      LMBCS_1 = 11;

    const
     int
      LMBCS_2 = 12;

    const
     int
      LMBCS_3 = 13;

    const
     int
      LMBCS_4 = 14;

    const
     int
      LMBCS_5 = 15;

    const
     int
      LMBCS_6 = 16;

    const
     int
      LMBCS_8 = 17;

    const
     int
      LMBCS_11 = 18;

    const
     int
      LMBCS_16 = 19;

    const
     int
      LMBCS_17 = 20;

    const
     int
      LMBCS_18 = 21;

    const
     int
      LMBCS_19 = 22;

    const
     int
      LMBCS_LAST = 22;

    const
     int
      HZ = 23;

    const
     int
      SCSU = 24;

    const
     int
      ISCII = 25;

    const
     int
      US_ASCII = 26;

    const
     int
      UTF7 = 27;

    const
     int
      BOCU1 = 28;

    const
     int
      UTF16 = 29;

    const
     int
      UTF32 = 30;

    const
     int
      CESU8 = 31;

    const
     int
      IMAP_MAILBOX = 32;


    /* Методы */
    
   public __construct(?string $destination_encoding = null, ?string $source_encoding = null)

    public convert(string $str, bool $reverse = false): string|false
public fromUCallback(    int $reason,    array $source,    int $codePoint,    int &$error): string|int|array|null
public static getAliases(string $name): array|false|null
public static getAvailable(): array
public getDestinationEncoding(): string|false|null
public getDestinationType(): int|false|null
public getErrorCode(): int
public getErrorMessage(): ?string
public getSourceEncoding(): string|false|null
public getSourceType(): int|false|null
public static getStandards(): ?array
public getSubstChars(): string|false|null
public static reasonText(int $reason): string
public setDestinationEncoding(string $encoding): bool
public setSourceEncoding(string $encoding): bool
public setSubstChars(string $chars): bool
public toUCallback(    int $reason,    string $source,    string $codeUnits,    int &$error): string|int|array|null
public static transcode(    string $str,    string $toEncoding,    string $fromEncoding,    ?array $options = null): string|false

   }
```

## Обумовлені константи

**`UConverter::REASON_UNASSIGNED`**

**`UConverter::REASON_ILLEGAL`**

**`UConverter::REASON_IRREGULAR`**

**`UConverter::REASON_RESET`**

**`UConverter::REASON_CLOSE`**

**`UConverter::REASON_CLONE`**

**`UConverter::UNSUPPORTED_CONVERTER`**

**`UConverter::SBCS`**

**`UConverter::DBCS`**

**`UConverter::MBCS`**

**`UConverter::LATIN_1`**

**`UConverter::UTF8`**

**`UConverter::UTF16_BigEndian`**

**`UConverter::UTF16_LittleEndian`**

**`UConverter::UTF32_BigEndian`**

**`UConverter::UTF32_LittleEndian`**

**`UConverter::EBCDIC_STATEFUL`**

**`UConverter::ISO_2022`**

**`UConverter::LMBCS_1`**

**`UConverter::LMBCS_2`**

**`UConverter::LMBCS_3`**

**`UConverter::LMBCS_4`**

**`UConverter::LMBCS_5`**

**`UConverter::LMBCS_6`**

**`UConverter::LMBCS_8`**

**`UConverter::LMBCS_11`**

**`UConverter::LMBCS_16`**

**`UConverter::LMBCS_17`**

**`UConverter::LMBCS_18`**

**`UConverter::LMBCS_19`**

**`UConverter::LMBCS_LAST`**

**`UConverter::HZ`**

**`UConverter::SCSU`**

**`UConverter::ISCII`**

**`UConverter::US_ASCII`**

**`UConverter::UTF7`**

**`UConverter::BOCU1`**

**`UConverter::UTF16`**

**`UConverter::UTF32`**

**`UConverter::CESU8`**

**`UConverter::IMAP_MAILBOX`**

## Зміст

-   [UConverter::construct](uconverter.construct.html) — Створити об'єкт UConverter
-   [UConverter::convert](uconverter.convert.html) — Конвертувати рядок з одного кодування в інше
-   [UConverter::fromUCallback](uconverter.fromucallback.html) — Callback-функція за промовчанням для "from"
-   [UConverter::getAliases](uconverter.getaliases.html) — Отримати псевдоніми для цього імені
-   [UConverter::getAvailable](uconverter.getavailable.html) — Отримати доступні імена канонічних конверторів
-   [UConverter::getDestinationEncoding](uconverter.getdestinationencoding.html) — Отримати кодування призначення
-   [UConverter::getDestinationType](uconverter.getdestinationtype.html) — Отримати тип конвертера призначення
-   [UConverter::getErrorCode](uconverter.geterrorcode.html) — Отримати код останньої помилки об'єкта
-   [UConverter::getErrorMessage](uconverter.geterrormessage.html) — Отримати останнє повідомлення про помилку в об'єкті
-   [UConverter::getSourceEncoding](uconverter.getsourceencoding.html) — Отримати вихідне кодування
-   [UConverter::getSourceType](uconverter.getsourcetype.html) — Отримати тип конвертера джерела
-   [UConverter::getStandards](uconverter.getstandards.html) — Отримати стандарти, пов'язані з іменами конвертерів
-   [UConverter::getSubstChars](uconverter.getsubstchars.html) — Отримати заміну символів
-   [UConverter::reasonText](uconverter.reasontext.html) — Отримати рядкове подання причини зворотного виклику
-   [UConverter::setDestinationEncoding](uconverter.setdestinationencoding.html) — Встановити кодування призначення
-   [UConverter::setSourceEncoding](uconverter.setsourceencoding.html) — Встановити вихідне кодування
-   [UConverter::setSubstChars](uconverter.setsubstchars.html) — Встановлення символів підстановки
-   [UConverter::toUCallback](uconverter.toucallback.html) - Callback-функція за промовчанням для "to"
-   [UConverter::transcode](uconverter.transcode.html) — Перетворює рядок з одного кодування символів на інший
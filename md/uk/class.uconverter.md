---
navigation:
  - intlpartsiterator.getbreakiterator.md: '« IntlPartsIterator::getBreakIterator'
  - uconverter.construct.md: 'UConverter::\_\_construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас UConverter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас UConverter

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

## Вступ

## Огляд класів

```classsynopsis

    
     class UConverter
     {

    /* Константы */
    
     public
     const
     int
      REASON_UNASSIGNED;

    public
     const
     int
      REASON_ILLEGAL;

    public
     const
     int
      REASON_IRREGULAR;

    public
     const
     int
      REASON_RESET;

    public
     const
     int
      REASON_CLOSE;

    public
     const
     int
      REASON_CLONE;

    public
     const
     int
      UNSUPPORTED_CONVERTER;

    public
     const
     int
      SBCS;

    public
     const
     int
      DBCS;

    public
     const
     int
      MBCS;

    public
     const
     int
      LATIN_1;

    public
     const
     int
      UTF8;

    public
     const
     int
      UTF16_BigEndian;

    public
     const
     int
      UTF16_LittleEndian;

    public
     const
     int
      UTF32_BigEndian;

    public
     const
     int
      UTF32_LittleEndian;

    public
     const
     int
      EBCDIC_STATEFUL;

    public
     const
     int
      ISO_2022;

    public
     const
     int
      LMBCS_1;

    public
     const
     int
      LMBCS_2;

    public
     const
     int
      LMBCS_3;

    public
     const
     int
      LMBCS_4;

    public
     const
     int
      LMBCS_5;

    public
     const
     int
      LMBCS_6;

    public
     const
     int
      LMBCS_8;

    public
     const
     int
      LMBCS_11;

    public
     const
     int
      LMBCS_16;

    public
     const
     int
      LMBCS_17;

    public
     const
     int
      LMBCS_18;

    public
     const
     int
      LMBCS_19;

    public
     const
     int
      LMBCS_LAST;

    public
     const
     int
      HZ;

    public
     const
     int
      SCSU;

    public
     const
     int
      ISCII;

    public
     const
     int
      US_ASCII;

    public
     const
     int
      UTF7;

    public
     const
     int
      BOCU1;

    public
     const
     int
      UTF16;

    public
     const
     int
      UTF32;

    public
     const
     int
      CESU8;

    public
     const
     int
      IMAP_MAILBOX;


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

-   [UConverter::\_\_construct](uconverter.construct.md)— Створити об'єкт UConverter
-   [UConverter::convert](uconverter.convert.md)— Конвертувати рядок з одного кодування в інше
-   [UConverter::fromUCallback](uconverter.fromucallback.md) — Callback-функція за промовчанням для "from"
-   [UConverter::getAliases](uconverter.getaliases.md)— Отримати псевдоніми для цього імені
-   [UConverter::getAvailable](uconverter.getavailable.md)— Отримати доступні імена канонічних конверторів
-   [UConverter::getDestinationEncoding](uconverter.getdestinationencoding.md)— Отримати кодування призначення
-   [UConverter::getDestinationType](uconverter.getdestinationtype.md)— Отримати тип конвертера призначення
-   [UConverter::getErrorCode](uconverter.geterrorcode.md)— Отримати код останньої помилки об'єкта
-   [UConverter::getErrorMessage](uconverter.geterrormessage.md)— Отримати останнє повідомлення про помилку в об'єкті
-   [UConverter::getSourceEncoding](uconverter.getsourceencoding.md)— Отримати вихідне кодування
-   [UConverter::getSourceType](uconverter.getsourcetype.md)— Отримати тип конвертера джерела
-   [UConverter::getStandards](uconverter.getstandards.md)— Отримати стандарти, пов'язані з іменами конвертерів
-   [UConverter::getSubstChars](uconverter.getsubstchars.md)— Отримати заміну символів
-   [UConverter::reasonText](uconverter.reasontext.md)— Отримати рядкове подання причини зворотного виклику
-   [UConverter::setDestinationEncoding](uconverter.setdestinationencoding.md)— Встановити кодування призначення
-   [UConverter::setSourceEncoding](uconverter.setsourceencoding.md)— Встановити вихідне кодування
-   [UConverter::setSubstChars](uconverter.setsubstchars.md)— Встановлення символів підстановки
-   [UConverter::toUCallback](uconverter.toucallback.md) - Callback-функція за промовчанням для "to"
-   [UConverter::transcode](uconverter.transcode.md)— Перетворює рядок з одного кодування символів на інший

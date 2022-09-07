---
navigation:
  - intlgregoriancalendar.setgregorianchange.md: '« IntlGregorianCalendar::setGregorianChange'
  - intltimezone.construct.md: 'IntlTimeZone::construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlTimeZone
---
# Клас IntlTimeZone

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlTimeZone
     
     {

    /* Constants */
    
     const
     int
      DISPLAY_SHORT = 1;

    const
     int
      DISPLAY_LONG = 2;


    /* Методы */
    
   private __construct()

    public static countEquivalentIDs(string $timezoneId): int|false
public static createDefault(): IntlTimeZone
public static createEnumeration(IntlTimeZone|string|int|float|null $countryOrRawOffset = null): IntlIterator|false
public static createTimeZone(string $timezoneId): ?IntlTimeZone
public static createTimeZoneIDEnumeration(int $type, ?string $region = null, ?int $rawOffset = null): IntlIterator|false
public static fromDateTimeZone(DateTimeZone $timezone): ?IntlTimeZone
public static getCanonicalID(string $timezoneId, bool &$isSystemId = null): string|false
public getDisplayName(bool $dst = false, int $style = IntlTimeZone::DISPLAY_LONG, ?string $locale = null): string|false
public getDSTSavings(): int
public static getEquivalentID(string $timezoneId, int $offset): string|false
public getErrorCode(): int|false
public getErrorMessage(): string|false
public static getGMT(): IntlTimeZone
public getID(): string|false
public static getIDForWindowsID(string $timezoneId, ?string $region = null): string|false
public getOffset(    float $timestamp,    bool $local,    int &$rawOffset,    int &$dstOffset): bool
public getRawOffset(): int
public static getRegion(string $timezoneId): string|false
public static getTZDataVersion(): string|false
public static getUnknown(): IntlTimeZone
public static getWindowsID(string $timezoneId): string|false
public hasSameRules(IntlTimeZone $other): bool
public toDateTimeZone(): DateTimeZone|false
public useDaylightTime(): bool

   }
```

## Обумовлені константи

**`IntlTimeZone::DISPLAY_SHORT`**

**`IntlTimeZone::DISPLAY_LONG`**

## Зміст

-   [IntlTimeZone::construct](intltimezone.construct.md) - Конструктор класу, який забороняє пряме створення екземпляра
-   [IntlTimeZone::countEquivalentIDs](intltimezone.countequivalentids.md) — Отримати кількість ідентифікаторів у групі схожих часових поясів, включаючи цей ідентифікатор
-   [IntlTimeZone::createDefault](intltimezone.createdefault.md) — Створити нову копію часового поясу за промовчанням для поточного хоста
-   [IntlTimeZone::createEnumeration](intltimezone.createenumeration.md) — Отримати перерахування з ідентифікаторів часових поясів за вказаною країною чи усунення
-   [IntlTimeZone::createTimeZone](intltimezone.createtimezone.md) — Створити об'єкт часового поясу по заданому ідентифікатору
-   [IntlTimeZone::createTimeZoneIDEnumeration](intltimezone.createtimezoneidenumeration.md) — Отримати перерахування з ідентифікаторів системних часових поясів за умовами фільтрації
-   [IntlTimeZone::fromDateTimeZone](intltimezone.fromdatetimezone.md) — Створити об'єкт часового поясу з DateTimeZone
-   [IntlTimeZone::getCanonicalID](intltimezone.getcanonicalid.md) — Отримати канонічний системний ідентифікатор часового поясу або нормалізований ідентифікатор часового поясу по заданому ідентифікатору часового поясу
-   [IntlTimeZone::getDisplayName](intltimezone.getdisplayname.md) — Отримати ім'я часового поясу для відображення користувача
-   [IntlTimeZone::getDSTSavings](intltimezone.getdstsavings.md) — Отримати кількість мілісекунд, яку потрібно додати до місцевого поясного часу, щоб отримати літній час
-   [IntlTimeZone::getEquivalentID](intltimezone.getequivalentid.md) — Отримати ідентифікатор у групі схожих часових поясів, включно із заданим ідентифікатором.
-   [IntlTimeZone::getErrorCode](intltimezone.geterrorcode.md) — Отримати останній код про помилку в об'єкті
-   [IntlTimeZone::getErrorMessage](intltimezone.geterrormessage.md) — Отримати останнє повідомлення про помилку в об'єкті
-   [IntlTimeZone::getGMT](intltimezone.getgmt.md) — Створити часовий пояс GMT (UTC)
-   [IntlTimeZone::getID](intltimezone.getid.md) — Отримати ідентифікатор часового поясу
-   [IntlTimeZone::getIDForWindowsID](intltimezone.getidforwindowsid.md) — Перетворити часовий пояс для Windows на системний часовий пояс
-   [IntlTimeZone::getOffset](intltimezone.getoffset.md) — Отримати необроблене значення часового поясу та усунення за Грінвічем (GMT) за заданим моментом часу
-   [IntlTimeZone::getRawOffset](intltimezone.getrawoffset.md) — Отримати необроблене значення зсуву за Грінвічем (GMT) без урахування літнього часу
-   [IntlTimeZone::getRegion](intltimezone.getregion.md) — Отримати код регіону, який відповідає заданому ідентифікатору системного часового поясу
-   [IntlTimeZone::getTZDataVersion](intltimezone.gettzdataversion.md) — Отримати версію даних про часовий пояс, який зараз використовується в ICU
-   [IntlTimeZone::getUnknown](intltimezone.getunknown.md) — Отримати невідомий часовий пояс (unknown)
-   [IntlTimeZone::getWindowsID](intltimezone.getwindowsid.md) — Перетворити часовий пояс на часовий пояс для Windows
-   [IntlTimeZone::hasSameRules](intltimezone.hassamerules.md) — Перевірити, що в іншому часовому поясі використовуються ті самі правила та зсуви, що й у першому заданому
-   [IntlTimeZone::toDateTimeZone](intltimezone.todatetimezone.md) — Перетворити на об'єкт DateTimeZone
-   [IntlTimeZone::useDaylightTime](intltimezone.usedaylighttime.md) — Перевірити, що в цьому часовому поясі використовується літній час

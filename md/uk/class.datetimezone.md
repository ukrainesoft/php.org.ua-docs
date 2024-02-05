---
navigation:
  - datetime.wakeup.md: '« DateTime::\_\_wakeup'
  - datetimezone.construct.md: 'DateTimeZone::\_\_construct »'
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateTimeZone
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateTimeZone

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

## Вступ

Подання часового поясу.

## Огляд класів

```classsynopsis

    
     class DateTimeZone
     {

    /* Константы */
    
     public
     const
     int
      AFRICA;

    public
     const
     int
      AMERICA;

    public
     const
     int
      ANTARCTICA;

    public
     const
     int
      ARCTIC;

    public
     const
     int
      ASIA;

    public
     const
     int
      ATLANTIC;

    public
     const
     int
      AUSTRALIA;

    public
     const
     int
      EUROPE;

    public
     const
     int
      INDIAN;

    public
     const
     int
      PACIFIC;

    public
     const
     int
      UTC;

    public
     const
     int
      ALL;

    public
     const
     int
      ALL_WITH_BC;

    public
     const
     int
      PER_COUNTRY;


    /* Методы */
    
   public __construct(string $timezone)

    public getLocation(): array|false
public getName(): string
public getOffset(DateTimeInterface $datetime): int
public getTransitions(int $timestampBegin = PHP_INT_MIN, int $timestampEnd = PHP_INT_MAX): array|false
public static listAbbreviations(): array
public static listIdentifiers(int $timezoneGroup = DateTimeZone::ALL, ?string $countryCode = null): array

   }
```

## Обумовлені константи

**`DateTimeZone::AFRICA`**

Часові пояси Африки.

**`DateTimeZone::AMERICA`**

Часові пояси Америки.

**`DateTimeZone::ANTARCTICA`**

Часові пояси Антарктики.

**`DateTimeZone::ARCTIC`**

Часові пояси Арктики.

**`DateTimeZone::ASIA`**

Часові пояси Азії.

**`DateTimeZone::ATLANTIC`**

Часові пояси Атлантики.

**`DateTimeZone::AUSTRALIA`**

Часові пояси Австралії.

**`DateTimeZone::EUROPE`**

Часові пояси Європи.

**`DateTimeZone::INDIAN`**

Часові пояси Індії.

**`DateTimeZone::PACIFIC`**

Часові пояси Тихого океану.

**`DateTimeZone::UTC`**

Часовий пояс UTC.

**`DateTimeZone::ALL`**

Усі часові пояси.

**`DateTimeZone::ALL_WITH_BC`**

Усі часові пояси, включаючи зворотно сумісні.

**`DateTimeZone::PER_COUNTRY`**

Число часових поясів на країну.

## Зміст

-   [DateTimeZone::\_\_construct](datetimezone.construct.md)— Створює новий об'єкт DateTimeZone
-   [DateTimeZone::getLocation](datetimezone.getlocation.md)— Повертає інформацію про місцезнаходження для часового поясу
-   [DateTimeZone::getName](datetimezone.getname.md)— Повертає ім'я часового поясу
-   [DateTimeZone::getOffset](datetimezone.getoffset.md)— Повертає усунення часового поясу від UTC (GMT)
-   [DateTimeZone::getTransitions](datetimezone.gettransitions.md)— Повертає всі переходи для часового поясу
-   [DateTimeZone::listAbbreviations](datetimezone.listabbreviations.md)— Повертає асоціативний масив, що містить прапор переходу на літній час, зміщення та ім'я часового поясу
-   [DateTimeZone::listIdentifiers](datetimezone.listidentifiers.md)— Повертає чисельно індексований масив із усіма ідентифікаторами часових поясів

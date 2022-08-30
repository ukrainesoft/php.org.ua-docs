Клас DateTimeZone

-   [« DateTime::wakeup](datetime.wakeup.md)
    
-   [DateTimeZone::construct »](datetimezone.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Дата/время](book.datetime.md)
    
-   Клас DateTimeZone
    

# Клас DateTimeZone

(PHP 5> = 5.2.0, PHP 7, PHP 8)

## Вступ

Подання часового поясу.

## Огляд класів

```classsynopsis

     
    

    
     
      class DateTimeZone
     
     {

    /* Константы */
    
     const
     int
      AFRICA = 1;

    const
     int
      AMERICA = 2;

    const
     int
      ANTARCTICA = 4;

    const
     int
      ARCTIC = 8;

    const
     int
      ASIA = 16;

    const
     int
      ATLANTIC = 32;

    const
     int
      AUSTRALIA = 64;

    const
     int
      EUROPE = 128;

    const
     int
      INDIAN = 256;

    const
     int
      PACIFIC = 512;

    const
     int
      UTC = 1024;

    const
     int
      ALL = 2047;

    const
     int
      ALL_WITH_BC = 4095;

    const
     int
      PER_COUNTRY = 4096;


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

-   [DateTimeZone::construct](datetimezone.construct.md) — Створює новий об'єкт DateTimeZone
-   [DateTimeZone::getLocation](datetimezone.getlocation.md) — Повертає інформацію про місцезнаходження для часового поясу
-   [DateTimeZone::getName](datetimezone.getname.md) — Повертає ім'я часового поясу
-   [DateTimeZone::getOffset](datetimezone.getoffset.md) — Повертає усунення часового поясу від UTC (GMT)
-   [DateTimeZone::getTransitions](datetimezone.gettransitions.md) — Повертає всі переходи для часового поясу
-   [DateTimeZone::listAbbreviations](datetimezone.listabbreviations.md) — Повертає асоціативний масив, що містить прапор переходу на літній час, зміщення та ім'я часового поясу
-   [DateTimeZone::listIdentifiers](datetimezone.listidentifiers.md) — Повертає чисельно індексований масив із усіма ідентифікаторами часових поясів
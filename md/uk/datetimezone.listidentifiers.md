---
navigation:
  - datetimezone.listabbreviations.md: '« DateTimeZone::listAbbreviations'
  - class.dateinterval.md: DateInterval »
  - index.md: PHP Manual
  - class.datetimezone.md: DateTimeZone
title: 'DateTimeZone::listIdentifiers'
---
# DateTimeZone::listIdentifiers

# timezoneidentifierslist

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeZone::listIdentifiers -- timezoneidentifierslist — Повертає чисельно індексований масив із усіма ідентифікаторами часових поясів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateTimeZone::listIdentifiers(int $timezoneGroup = DateTimeZone::ALL, ?string $countryCode = null): array
```

Процедурний стиль

```methodsynopsis
timezone_identifiers_list(int $timezoneGroup = DateTimeZone::ALL, ?string $countryCode = null): array
```

### Список параметрів

`timezoneGroup`

Одна з констант класу [DateTimeZone](class.datetimezone.md) (або комбінація їх).

`countryCode`

Дволітерний код країни у верхньому регістрі, сумісний із ISO 3166-1.

> **Зауваження**: Ця опція використовується тільки тоді, коли параметр `timezoneGroup` встановлений в **`DateTimeZone::PER_COUNTRY`**

### Значення, що повертаються

Повертає масив ідентифікаторів часових поясів. Повертаються лише не застарілі елементи. Щоб отримати всі, включаючи застарілі ідентифікатори часових поясів, використовуйте `DateTimeZone::ALL_WITH_BC` як значення для параметра `countryCode`

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії, у разі виникнення помилки поверталося **`false`** |
|  | `countryCode` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **DateTimeZone::listIdentifiers()****

```php
<?php
$timezone_identifiers = DateTimeZone::listIdentifiers();
for ($i=0; $i < 5; $i++) {
    echo "$timezone_identifiers[$i]\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Africa/Abidjan
Africa/Accra
Africa/Addis_Ababa
Africa/Algiers
Africa/Asmara
```

**Приклад #2 Перелік ідентифікаторів для конкретного регіону**

```php
<?php
$timezone_identifiers = DateTimeZone::listIdentifiers( DateTimeZone::ASIA );
for ($i=0; $i < 5; $i++) {
    echo "$timezone_identifiers[$i]\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Asia/Aden
Asia/Almaty
Asia/Amman
Asia/Anadyr
Asia/Aqtau
```

**Приклад #3 Перелік ідентифікаторів для кількох регіонів**

```php
<?php
$timezone_identifiers = DateTimeZone::listIdentifiers( DateTimeZone::ASIA | DateTimeZone::PACIFIC );
echo join( ', ', $timezone_identifiers );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Asia/Aden, Asia/Almaty, Asia/Amman, Asia/Anadyr, Asia/Aqtau, Asia/Aqtobe,
Asia/Ashgabat, Asia/Atyrau, Asia/Baghdad, Asia/Bahrain, Asia/Baku,
Asia/Bangkok, Asia/Barnaul, Asia/Beirut, Asia/Bishkek, Asia/Brunei,
Asia/Chita, Asia/Choibalsan, Asia/Colombo, Asia/Damascus, Asia/Dhaka,
Asia/Dili, Asia/Dubai, Asia/Dushanbe, Asia/Famagusta, Asia/Gaza, Asia/Hebron,
Asia/Ho_Chi_Minh, Asia/Hong_Kong, Asia/Hovd, Asia/Irkutsk, Asia/Jakarta,
Asia/Jayapura, Asia/Jerusalem, Asia/Kabul, Asia/Kamchatka, Asia/Karachi,
Asia/Kathmandu, Asia/Khandyga, Asia/Kolkata, Asia/Krasnoyarsk,
Asia/Kuala_Lumpur, Asia/Kuching, Asia/Kuwait, Asia/Macau, Asia/Magadan,
Asia/Makassar, Asia/Manila, Asia/Muscat, Asia/Nicosia, Asia/Novokuznetsk,
Asia/Novosibirsk, Asia/Omsk, Asia/Oral, Asia/Phnom_Penh, Asia/Pontianak,
Asia/Pyongyang, Asia/Qatar, Asia/Qostanay, Asia/Qyzylorda, Asia/Riyadh,
Asia/Sakhalin, Asia/Samarkand, Asia/Seoul, Asia/Shanghai, Asia/Singapore,
Asia/Srednekolymsk, Asia/Taipei, Asia/Tashkent, Asia/Tbilisi, Asia/Tehran,
Asia/Thimphu, Asia/Tokyo, Asia/Tomsk, Asia/Ulaanbaatar, Asia/Urumqi,
Asia/Ust-Nera, Asia/Vientiane, Asia/Vladivostok, Asia/Yakutsk, Asia/Yangon,
Asia/Yekaterinburg, Asia/Yerevan, Pacific/Apia, Pacific/Auckland,
Pacific/Bougainville, Pacific/Chatham, Pacific/Chuuk, Pacific/Easter,
Pacific/Efate, Pacific/Fakaofo, Pacific/Fiji, Pacific/Funafuti,
Pacific/Galapagos, Pacific/Gambier, Pacific/Guadalcanal, Pacific/Guam,
Pacific/Honolulu, Pacific/Kanton, Pacific/Kiritimati, Pacific/Kosrae,
Pacific/Kwajalein, Pacific/Majuro, Pacific/Marquesas, Pacific/Midway,
Pacific/Nauru, Pacific/Niue, Pacific/Norfolk, Pacific/Noumea,
Pacific/Pago_Pago, Pacific/Palau, Pacific/Pitcairn, Pacific/Pohnpei,
Pacific/Port_Moresby, Pacific/Rarotonga, Pacific/Saipan, Pacific/Tahiti,
Pacific/Tarawa, Pacific/Tongatapu, Pacific/Wake, Pacific/Wallis
```

**Приклад #4 Перелік ідентифікаторів для однієї країни**

```php
<?php
$timezone_identifiers = DateTimeZone::listIdentifiers( DateTimeZone::PER_COUNTRY, "UA" );
foreach( $timezone_identifiers as $identifier ) {
    echo "$identifier\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Europe/Kyiv
Europe/Simferopol
Europe/Uzhgorod
Europe/Zaporozhye
```

### Дивіться також

-   [timezoneabbreviationslist()](function.timezone-abbreviations-list.md) - Псевдонім DateTimeZone::listAbbreviations

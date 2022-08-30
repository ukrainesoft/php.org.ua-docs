Налаштування під час виконання

-   [« Установка](datetime.installation.html)
    
-   [Типи ресурсів »](datetime.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Встановлення та налаштування](datetime.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Налаштування конфігурації дати/часу**

| Имя                                                                             | По умолчанию | Место изменения | Список изменений |
|---------------------------------------------------------------------------------|--------------|-----------------|------------------|
| [date.defaultlatitude](datetime.configuration.html#ini.date.default-latitude)   | "31.7667"    | PHPINIALL       |                  |
| [date.defaultlongitude](datetime.configuration.html#ini.date.default-longitude) | "35.2333"    | PHPINIALL       |                  |
| [date.sunrisezenith](datetime.configuration.html#ini.date.sunrise-zenith)       | "90.583333"  | PHPINIALL       |                  |
| [date.sunsetzenith](datetime.configuration.html#ini.date.sunset-zenith)         | "90.583333"  | PHPINIALL       |                  |
| [date.timezone](datetime.configuration.html#ini.date.timezone)                  | "UTC"        | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`date.default_latitude` float

За замовчуванням ширина. в діапазоні від `0` на екваторі до `+90` на північ і `-90` на південь.

`date.default_longitude` float

Довгота за замовчуванням. в діапазоні від `0` на нульовому меридіані до `+180` на схід та `-180` на захід.

`date.sunrise_zenith` float

Кут, під яким сонце світить під час сходу.

`date.sunset_zenith` float

Кут, під яким сонце світить під час заходу сонця.

`date.timezone` string

Часовий пояс, який використовується за умовчанням всіма функціями дати/часу. Порядок пріоритету часових поясів, що використовуються, описаний на сторінці [datedefaulttimezoneget()](function.date-default-timezone-get.html). Дивіться також [Список підтримуваних часових поясів](timezones.html)

> **Зауваження**: Перші чотири опції налаштування в даний час використовуються тільки у функціях [datesunrise()](function.date-sunrise.html) і [datesunset()](function.date-sunset.html)
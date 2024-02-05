---
navigation:
  - datetime.installation.md: « Встановлення
  - datetime.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - datetime.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Налаштування конфігурації дати/часу**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [date.default\_latitude](datetime.configuration.md#ini.date.default-latitude) | "31.7667" | **`INI_ALL`** |  |
| [date.default\_longitude](datetime.configuration.md#ini.date.default-longitude) | "35.2333" | **`INI_ALL`** |  |
| [date.sunrise\_zenith](datetime.configuration.md#ini.date.sunrise-zenith) | "90.833333" | **`INI_ALL`** | До PHP 8.0.0 значення за промовчанням було "90.583333". |
| [date.sunset\_zenith](datetime.configuration.md#ini.date.sunset-zenith) | "90.833333" | **`INI_ALL`** | До PHP 8.0.0 значення за промовчанням було "90.583333". |
| [date.timezone](datetime.configuration.md#ini.date.timezone) | "UTC" | **`INI_ALL`** | Починаючи з PHP 8.2, під час встановлення неприпустимого значення або порожнього рядка видається попередження. |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`date.default_latitude`float

Широта по умолчанию. в диапазоне от на екваторі до `+90` на північ і `-90`к югу.

`date.default_longitude`float

Долгота по умолчанию. в диапазоне от на нулевом меридиане до`+180` на схід та `-180`на запад.

`date.sunrise_zenith`float

Кут, під яким сонце світить під час сходу.

Значення за замовчуванням становить 90 ° 50 '. Додаткові 50' обумовлені двома компонентами: радіусом Сонця, що становить 16' та атмосферною рефракцією, яка становить 34'.

`date.sunset_zenith`float

Кут, під яким сонце світить під час заходу сонця.

`date.timezone`string

Часовий пояс, який використовується за умовчанням всіма функціями дати/часу. Порядок пріоритету часових поясів, що використовуються, описаний на сторінці [date\_default\_timezone\_get()](function.date-default-timezone-get.md)Смотрите также [Список підтримуваних часових поясів](timezones.md)

> **Зауваження**: Перші чотири опції налаштування в даний час використовуються тільки у функціях [date\_sunrise()](function.date-sunrise.md) і [date\_sunset()](function.date-sunset.md)

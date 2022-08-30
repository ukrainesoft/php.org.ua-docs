Інтерфейс DateTimeInterface

-   [« DateTimeImmutable::sub](datetimeimmutable.sub.md)
    
-   [DateTimeInterface::diff »](datetime.diff.md)
    
-   [PHP Manual](index.md)
    
-   [Дата/время](book.datetime.md)
    
-   Інтерфейс DateTimeInterface
    

# Інтерфейс DateTimeInterface

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **DateTimeInterface** узагальнює роботу [DateTimeImmutable](class.datetimeimmutable.md) або [DateTime](class.datetime.md). Неможливо реалізувати цей інтерфейс з класом користувача.

Загальні константи, які дозволяють форматувати об'єкти [DateTimeImmutable](class.datetimeimmutable.md) або [DateTime](class.datetime.md) за допомогою [DateTimeImmutable::format()](datetime.format.md) і [DateTime::format()](datetime.format.md) також визначено у цьому інтерфейсі.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface DateTimeInterface {

    /* Константы */
    
     const
     string
      ATOM = "Y-m-d\TH:i:sP";

    const
     string
      COOKIE = "l, d-M-Y H:i:s T";

    const
     string
      ISO8601 = "Y-m-d\TH:i:sO";

    const
     string
      ISO8601_EXPANDED = "X-m-d\TH:i:sP";

    const
     string
      RFC822 = "D, d M y H:i:s O";

    const
     string
      RFC850 = "l, d-M-y H:i:s T";

    const
     string
      RFC1036 = "D, d M y H:i:s O";

    const
     string
      RFC1123 = "D, d M Y H:i:s O";

    const
     string
      RFC7231 = "D, d M Y H:i:s \G\M\T";

    const
     string
      RFC2822 = "D, d M Y H:i:s O";

    const
     string
      RFC3339 = "Y-m-d\TH:i:sP";

    const
     string
      RFC3339_EXTENDED = "Y-m-d\TH:i:s.vP";

    const
     string
      RSS = "D, d M Y H:i:s O";

    const
     string
      W3C = "Y-m-d\TH:i:sP";


    /* Методы */
    
   public diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
public format(string $format): string
public getOffset(): int
public getTimestamp(): int
public getTimezone(): DateTimeZone|false
public __wakeup(): void

   }
```

## Обумовлені константи

**`DateTime::ATOM`**

**`DATE_ATOM`**

Atom (приклад: 2005-08-15T15:52:01+00:00)

**`DateTime::COOKIE`**

**`DATE_COOKIE`**

HTTP Cookies (приклад: Monday, 15-Aug-05 15:52:01 UTC)

**`DateTime::ISO8601`**

**`DATE_ISO8601`**

ISO-8601 (приклад: 2005-08-15T15:52:01+0000)

> **Зауваження**: Цей формат не сумісний із ISO-8601, але залишається для зворотної сумісності. Замість нього використовуйте **`DateTimeInterface::ISO8601_EXPANDED`** або **`DateTimeInterface::ATOM`** для сумісності із ISO-8601.

**`DateTimeInterface::ISO8601_EXPANDED`**

**`DATE_ISO8601_EXPANDED`**

ISO-8601 Expanded (приклад: +10191-07-26T08:59:52+01:00)

> **Зауваження**: Формат дозволяє використовувати діапазони років, що виходять за межі звичайного діапазону ISO-8601 (`0000``9999`), завжди включаючи знак значок. Він також враховує, що частина часового поясу (`+01:00`) сумісна з ISO-8601.

**`DateTime::RFC822`**

**`DATE_RFC822`**

RFC 822 (приклад: Mon, 15 Aug 05 15:52:01 +0000)

**`DateTime::RFC850`**

**`DATE_RFC850`**

RFC 850 (приклад: Monday, 15-Aug-05 15:52:01 UTC)

**`DateTime::RFC1036`**

**`DATE_RFC1036`**

RFC 1036 (приклад: Mon, 15 Aug 05 15:52:01 +0000)

**`DateTime::RFC1123`**

**`DATE_RFC1123`**

RFC 1123 (приклад: Mon, 15 Aug 2005 15:52:01 +0000)

**`DateTimeInterface::RFC7231`**

**`DATE_RFC7231`**

RFC 7231 (з версії PHP 7.0.19 та 7.1.5) (приклад: Sat, 30 Apr 2016 17:52:13 GMT)

**`DateTime::RFC2822`**

**`DATE_RFC2822`**

RFC 2822 (приклад: Mon, 15 Aug 2005 15:52:01 +0000)

**`DateTime::RFC3339`**

**`DATE_RFC3339`**

Теж, що й **`DATE_ATOM`**

**`DateTime::RFC3339_EXTENDED`**

**`DATE_RFC3339_EXTENDED`**

Формат RFC 3339 EXTENDED (приклад: 2005-08-15T15:52:01.000+00:00)

**`DateTime::RSS`**

**`DATE_RSS`**

RSS (приклад: Mon, 15 Aug 2005 15:52:01 +0000)

**`DateTime::W3C`**

**`DATE_W3C`**

World Wide Web Consortium (приклад: 2005-08-15T15:52:01+00:00)

## список змін

| Версия | Описание |
| --- | --- |
|  | Додано константу DateTimeInterface::ISO8601EXPANDED. |
|  | Константи класу тепер [DateTime](class.datetime.md) визначено в **DateTimeInterface** |

## Зміст

-   [DateTimeInterface::diff](datetime.diff.md) — Повертає різницю між двома об'єктами DateTime
-   [DateTimeInterface::format](datetime.format.md) — Повертає дату, відформатовану згідно з переданим форматом
-   [DateTimeInterface::getOffset](datetime.getoffset.md) — Повертає усунення часового поясу
-   [DateTimeInterface::getTimestamp](datetime.gettimestamp.md) — Повертає тимчасову мітку Unix
-   [DateTimeInterface::getTimezone](datetime.gettimezone.md) — Повертає часовий пояс щодо поточного значення DateTime
-   [DateTime::wakeup](datetime.wakeup.md) - Обробник wakeup
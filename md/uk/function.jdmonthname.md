---
navigation:
  - function.jddayofweek.md: « jddayofweek
  - function.jdtofrench.md: jdtofrench »
  - index.md: PHP Manual
  - ref.calendar.md: Календар
title: jdmonthname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# jdmonthname

(PHP 4, PHP 5, PHP 7, PHP 8)

jdmonthname — Повертає назву місяця

### Опис

```methodsynopsis
jdmonthname(int $julian_day, int $mode): string
```

Повертає рядок, що містить назву місяця . `mode` задає режим роботи функції перетворення з числа днів у юліанському літочисленні, а також визначає тип значення назви місяця, що повертається.

**Режими роботи**

| Режим | Название месяца | Значения |
| --- | --- | --- |
| **`CAL_MONTH_GREGORIAN_SHORT`** | Григоріанське - скорочене | Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec |
| **`CAL_MONTH_GREGORIAN_LONG`** | Григоріанське | January, February, March, April, May, June, July, August, September, October, November, December |
| **`CAL_MONTH_JULIAN_SHORT`** | Юліанське - скорочене | Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec |
| **`CAL_MONTH_JULIAN_LONG`** | Юліанське | January, February, March, April, May, June, July, August, September, October, November, December |
| **`CAL_MONTH_JEWISH`** | Єврейське | Tishri, Heshvan, Kislev, Tevet, Shevat, Adar, Adar I, Adar II, Nisan, Iyyar, Sivan, Tammuz, Av, Elul |
| **`CAL_MONTH_FRENCH`** | Французьке республіканське | Vendemiaire, Brumaire, Frimaire, Nivose, Pluviose, Ventose, Germinal, Floreal, Prairial, Messidor, Thermidor, Fructidor, Extra |

### Список параметрів

`jday`

Число днів у юліанському літочисленні, яке потрібно перетворити

`mode`

Режим календаря (див. таблицю вище)

### Значення, що повертаються

Назва місяця для заданого Юліанського Дня, що відповідає календарю `mode`

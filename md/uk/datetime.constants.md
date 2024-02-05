---
navigation:
  - datetime.resources.md: « Типи ресурсів
  - datetime.examples.md: Приклади »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

[Константи `DATE_`](class.datetimeinterface.md#datetimeinterface.constants.types) пропонують стандартні уявлення дати, які можуть бути використані разом із функціями форматування дати (наприклад [date()](function.date.md)

Наступні константи визначають формат повертається функціями [date\_sunrise()](function.date-sunrise.md) і [date\_sunset()](function.date-sunset.md)

**`SUNFUNCS_RET_TIMESTAMP`**(int)

Час у секундах від початку епохи Unix

**`SUNFUNCS_RET_STRING`**(int)

Годинник:хвилини (наприклад: 08:02)

**`SUNFUNCS_RET_DOUBLE`**(int)

Годинник як число з плаваючою точкою (наприклад: 8.75)

- [« trader_cdlmatchinglow](function.trader-cdlmatchinglow.md)
- [trader_cdlmorningdojistar »](function.trader-cdlmorningdojistar.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Фігура Підстилка

#trader_cdlmathold

(PECL trader \>= 0.2.0)

trader_cdlmathold — Фігура Підстилка

### Опис

**trader_cdlmathold**(
array `$open`,
array `$high`,
array `$low`,
array `$close`,
float `$penetration` = ?
): array

### Список параметрів

`open`
Ціна відкриття масив реальних значень.

`high`
Висока вартість, масив реальних значень.

`low`
Низька вартість, масив реальних значень.

`close`
Ціна закриття, масив реальних значень.

`penetration`
Відсоток проникнення однієї свічки всередині іншої свічки.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.

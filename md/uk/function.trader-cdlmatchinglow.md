- [« trader_cdlmarubozu](function.trader-cdlmarubozu.md)
- [trader_cdlmathold »](function.trader-cdlmathold.md)

- [PHP Manual](index.md)
- [Функції Trader](ref.trader.md)
- Свічкова модель "Збіг за нижнім рівнем"

#trader_cdlmatchinglow

(PECL trader \>= 0.2.0)

trader_cdlmatchinglow — Свічкова модель "Збіг за нижнім рівнем"

### Опис

**trader_cdlmatchinglow**(
array `$open`,
array `$high`,
array `$low`,
array `$close`
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

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі
виникнення помилки.

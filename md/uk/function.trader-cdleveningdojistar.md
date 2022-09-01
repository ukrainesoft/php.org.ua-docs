---
navigation:
  - function.trader-cdlengulfing.html: « tradercdlengulfing
  - function.trader-cdleveningstar.html: tradercdleveningstar »
  - index.html: PHP Manual
  - ref.trader.html: Функции Trader
title: tradercdleveningdojistar
---
# tradercdleveningdojistar

(PECL trader >= 0.2.0)

tradercdleveningdojistar — Вечірня дожі-зірка

### Опис

```methodsynopsis
trader_cdleveningdojistar(    array $open,    array $high,    array $low,    array $close,    float $penetration = ?): array
```

### Список параметрів

`open`

Ціна відкриття масив реальних значень.

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`penetration`

Відсоток проникнення однієї свічки всередині іншої свічки.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.

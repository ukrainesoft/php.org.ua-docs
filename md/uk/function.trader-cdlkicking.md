---
navigation:
  - function.trader-cdlinvertedhammer.html: « tradercdlinvertedhammer
  - function.trader-cdlkickingbylength.html: tradercdlkickingbylength »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: tradercdlkicking
---
# tradercdlkicking

(PECL trader >= 0.2.0)

tradercdlkicking - Свічкова модель "Високий стрибок"

### Опис

```methodsynopsis
trader_cdlkicking(    array $open,    array $high,    array $low,    array $close): array
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

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.

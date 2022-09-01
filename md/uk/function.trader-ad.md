---
navigation:
  - function.trader-acos.html: « traderacos
  - function.trader-add.html: traderadd »
  - index.md: PHP Manual
  - ref.trader.md: Функции Trader
title: traderпекло
---
# traderпекло

(PECL trader >= 0.2.0)

traderad — Індикатор Чайкіна Накопичення/Розпродаж

### Опис

```methodsynopsis
trader_ad(    array $high,    array $low,    array $close,    array $volume): array
```

### Список параметрів

`high`

Висока ціна, масив реальних значень.

`low`

Низька вартість, масив реальних значень.

`close`

Ціна закриття, масив реальних значень.

`volume`

Обсяг торгів, масив реальних значень.

### Значення, що повертаються

Повертає масив з обчисленими даними або false у разі виникнення помилки.

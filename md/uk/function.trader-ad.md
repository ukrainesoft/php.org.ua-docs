---
navigation:
  - function.trader-acos.md: « trader\_acos
  - function.trader-add.md: trader\_add »
  - index.md: PHP Manual
  - ref.trader.md: Функції Trader
title: trader\_ad
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trader\_ad

(PECL trader >= 0.2.0)

trader\_ad — Індикатор Чайкіна Накопичення/Розпродаж

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

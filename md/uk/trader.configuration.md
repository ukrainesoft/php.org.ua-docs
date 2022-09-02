---
navigation:
  - trader.installation.md: « Установка
  - trader.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - trader.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Trader**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [trader.realprecision](trader.configuration.md#ini.trader.real-precision) |  | PHPINIALL | З версії trader 0.2.1 |
| [trader.realroundmode](trader.configuration.md#ini.trader.real-round-mode) | HALFDOWN | PHPINIALL | З версії trader 0.3.0 |

Коротке пояснення конфігураційних директив.

`trader.real_precision` int

Всі значення в масивах, що повертаються, будуть округлені до цієї точності. Однак розрахунки всередині TA-Lib відбуваються з неокругленими значеннями.

`trader.real_round_mode` string

Контролює реальну політику округлення trader. Допустимі значення: `HALF_UP` `HALF_DOWN` `HALF_EVEN` і `HALF_ODD`. Поведінка ідентична функції [round()](function.round.md), що використовується з аргументом mode.

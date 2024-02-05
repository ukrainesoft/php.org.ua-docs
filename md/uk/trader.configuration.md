---
navigation:
  - trader.installation.md: « Встановлення
  - trader.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - trader.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Trader**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [trader.real\_precision](trader.configuration.md#ini.trader.real-precision) | 3 | **`INI_ALL`** | З версії trader 0.2.1 |
| [trader.real\_round\_mode](trader.configuration.md#ini.trader.real-round-mode) | HALF\_DOWN | **`INI_ALL`** | З версії trader 0.3.0 |

Коротке пояснення конфігураційних директив.

`trader.real_precision`int

Всі значення в масивах, що повертаються, будуть округлені до цієї точності. Однак розрахунки всередині TA-Lib відбуваються з неокругленими значеннями.

`trader.real_round_mode`string

Контролює реальну політику округлення trader. Допустимі значення: `HALF_UP` `HALF_DOWN` `HALF_EVEN`и`HALF_ODD`. Поведінка ідентична функції [round()](function.round.md), що використовується з аргументом mode.

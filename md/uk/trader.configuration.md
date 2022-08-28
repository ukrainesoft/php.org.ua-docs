Налаштування під час виконання

-   [« Установка](trader.installation.html)
    
-   [Предопределённые константы »](trader.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](trader.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Trader**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [trader.real\_precision](trader.configuration.html#ini.trader.real-precision) |  | PHPINIALL | З версії trader 0.2.1 |
| [trader.real\_round\_mode](trader.configuration.html#ini.trader.real-round-mode) | HALFDOWN | PHPINIALL | З версії trader 0.3.0 |

Коротке пояснення конфігураційних директив.

`trader.real_precision` int

Всі значення в масивах, що повертаються, будуть округлені до цієї точності. Однак розрахунки всередині TA-Lib відбуваються з неокругленими значеннями.

`trader.real_round_mode` string

Контролює реальну політику округлення trader. Допустимі значення: `HALF_UP` `HALF_DOWN` `HALF_EVEN` і `HALF_ODD`. Поведінка ідентична функції [round()](function.round.html), що використовується з аргументом mode.
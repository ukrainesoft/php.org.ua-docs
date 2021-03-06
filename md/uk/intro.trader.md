- [«Trader](book.trader.md)
- [Встановлення та налаштування »](trader.setup.md)

- [PHP Manual](index.md)
- [Trader](book.trader.md)
-   Вступ

# Вступ

Модуль trader – це безкоштовна фондова бібліотека з відкритим вихідним
кодом, що базується на TA-Lib. Він призначений для розробників
програмного забезпечення для торгівлі, яким необхідний технічний
аналіз даних ринку. Поряд із багатьма індикаторами, такими
як ADX, MACD, RSI, Stochastic, TRIX, є розпізнавання свічкових
моделей та кілька векторних арифметичних та алгебраїчних функцій.

Розрахунки можна зробити у двох режимах – TA-Lib та Metastock. Зміна
режиму за допомогою [trader_set_compat()](function.trader-set-compat.md)
вплине роботу деяких функцій трейдера.

Деякі функції трейдера дають різні результати залежно від
"відправної точки" задіяних даних. Це часто називають функцією,
має спогади. Прикладом такої функції є експонентна
ковзна середня. Можна керувати нестабільним періодом (обсягом
даних для видалення), використовуючи
[trader_set_unstable_period()](function.trader-set-unstable-period.md).

Розширену документацію за індикаторами, формулами та реалізаціями на
інших мовах програмування можна знайти за посиланням
[»Tadoc.org](http://tadoc.org/).

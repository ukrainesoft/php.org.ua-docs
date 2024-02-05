---
navigation:
  - language.expressions.md: « Вирази
  - language.operators.precedence.md: Пріоритет »
  - index.md: PHP Manual
  - langref.md: Довідник мови
title: Оператори
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Оператори

## Зміст

-   [Пріоритет](language.operators.precedence.md)
-   [Арифметика](language.operators.arithmetic.md)
-   [Інкремент та декремент](language.operators.increment.md)
-   [Привласнення](language.operators.assignment.md)
-   [Побітові оператори](language.operators.bitwise.md)
-   [Порівняння](language.operators.comparison.md)
-   [Управління помилками](language.operators.errorcontrol.md)
-   [Виконання](language.operators.execution.md)
-   [Логіка](language.operators.logical.md)
-   [Рядки](language.operators.string.md)
-   [Масиви](language.operators.array.md)
-   [Перевірка типу](language.operators.type.md)

Оператором називається щось, що набуває одного або більше значень (або виразів, якщо говорити на жаргоні програмування), і обчислює нове значення (так, всю конструкцію можна розглядати як вираз).

Оператори можна згрупувати за кількістю значень, що приймаються ними. Унарні оператори набувають лише одного значення, наприклад, `!` [оператор логічного заперечення](language.operators.logical.md)) или`++` [інкремент](language.operators.increment.md)). Бінарні оператори набувають двох значень; це, наприклад, знайомі всім [арифметичні оператори](language.operators.arithmetic.md) `+` (плюс) и`-` (мінус), більшість підтримуваних в PHP операторів входить в цю категорію. І наостанок, існує лише один [тернарний оператор](language.operators.comparison.md#language.operators.comparison.ternary) `? :`, Що приймає три значення, зазвичай про нього говорять просто - «тернарний оператор» (хоча, можливо, більш точною назвою було б «умовний оператор»).

Весь список PHP-операторів перерахований у розділі «[Пріоритет оператора](language.operators.precedence.md)». У цьому розділі також описано порядок виконання операторів та їхню асоціативність, які точно визначають, як обчислюються вирази з кількома різними операторами.

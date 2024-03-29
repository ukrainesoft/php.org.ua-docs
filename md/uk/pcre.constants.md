---
navigation:
  - pcre.resources.md: « Типи ресурсів
  - pcre.examples.md: Приклади »
  - index.md: PHP Manual
  - book.pcre.md: PCRE
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**Константи PREG**

| Константы | Опис | С версии |
| --- | --- | --- |
| **`PREG_PATTERN_ORDER`**(int) | Змінює порядок елементів у результуючому масиві так, щоб елемент $matches\[ \] містив повні входження шаблону, елемент $matches\[ \] - всі входження першої взятої у круглі дужки підмаски тощо. буд. Цей прапор вказують лише за виклику функції [preg\_match\_all()](function.preg-match-all.md) |  |
| **`PREG_SET_ORDER`**(int) | Змінює порядок елементів у результуючому масиві так, щоб елемент $matches\[ \] містив перший набір входження (повне входження, входження першої підмаски, укладеної в круглі дужки...), аналогічно елемент $matches\[ \] - другий набір входжень і т. д. Цей прапор вказують тільки при виклику функції [preg\_match\_all()](function.preg-match-all.md) |  |
| **`PREG_OFFSET_CAPTURE`**(int) | Дивіться опис прапора **`PREG_SPLIT_OFFSET_CAPTURE`** |  |
| **`PREG_SPLIT_NO_EMPTY`**(int) | Якщо цей прапор вказано, функція [preg\_split()](function.preg-split.md) поверне лише непусті підрядки. |  |
| **`PREG_SPLIT_DELIM_CAPTURE`**(int) | Якщо цей прапор вказано, то функція [preg\_split()](function.preg-split.md) також повертає вираз, укладений у шаблоні роздільника у круглі дужки. |  |
| **`PREG_SPLIT_OFFSET_CAPTURE`**(int) | Якщо цей прапор вказано, для кожного знайденого підрядка буде вказано її позицію у вихідному рядку. Коли вказують цей прапор, враховують, що він змінює формат даних, що повертаються: кожне входження повертається у вигляді масиву, в нульовому елементі якого міститься знайдена підрядка, а в першому — зміщення. Цей прапор вказують лише за виклику функції [preg\_split()](function.preg-split.md) |  |
| **`PREG_UNMATCHED_AS_NULL`**(int) | Цей прапор вказує функціям [preg\_match()](function.preg-match.md) і [preg\_match\_all()](function.preg-match-all.md) включати несхожі підмаски в змінній $matches у вигляді значень **`null`**. . Без цього прапора підмаски, що не збігаються, відображаються як порожні рядки, як би не було знайдено збігів. Установка цього прапора дозволяє проводити різницю між двома цими випадками. | 7.2.0 |
| **`PREG_NO_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md)якщо помилок немає. | 5.2.0 |
| **`PREG_INTERNAL_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md), якщо виникла внутрішня помилка PCRE. | 5.2.0 |
| **`PREG_BACKTRACK_LIMIT_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md), якщо [ліміт зворотних посилань](pcre.configuration.md#ini.pcre.backtrack-limit) був вичерпаний. | 5.2.0 |
| **`PREG_RECURSION_LIMIT_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md), якщо [ліміт рекурсії](pcre.configuration.md#ini.pcre.recursion-limit) був вичерпаний. | 5.2.0 |
| **`PREG_BAD_UTF8_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md)якщо остання помилка була викликана неправильними даними UTF-8 (тільки при запуску регулярного виразу [у режимі UTF-8](reference.pcre.pattern.modifiers.md) | 5.2.0 |
| **`PREG_BAD_UTF8_OFFSET_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md)якщо зсув не відповідає початку коректної кодової точки UTF-8 (тільки при запуску [у режимі UTF-8](reference.pcre.pattern.modifiers.md) | 5.3.0 |
| **`PREG_JIT_STACKLIMIT_ERROR`**(int) | Повертається функцією [preg\_last\_error()](function.preg-last-error.md), якщо остання функція PCRE завершилася невдало через ліміт стека JIT. | 7.0.0 |
| **`PCRE_VERSION`**(string) | Версія та дата релізу PCRE (наприклад, «`7.0 18-Dec-2006`»). | 5.2.4 |

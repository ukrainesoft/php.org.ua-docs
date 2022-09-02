---
navigation:
  - array.resources.md: « Типи ресурсів
  - array.sorting.md: Сортування масивів »
  - index.md: PHP Manual
  - book.array.md: Масиви
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**`CASE_LOWER`** (int)

**`CASE_LOWER`** використовується з [arraychangekeycase()](function.array-change-key-case.md) для конвертації ключів масиву у нижній регістр. Це дія за умовчанням для [arraychangekeycase()](function.array-change-key-case.md)

**`CASE_UPPER`** (int)

**`CASE_UPPER`** використовується c [arraychangekeycase()](function.array-change-key-case.md) для конвертації ключів масиву у верхній регістр.

Прапори, що змінюють порядок сортування:

**`SORT_ASC`** (int)

**`SORT_ASC`** використовується з [arraymultisort()](function.array-multisort.md) для сортування у порядку зростання.

**`SORT_DESC`** (int)

**`SORT_DESC`** використовується з [arraymultisort()](function.array-multisort.md) для сортування в порядку зменшення.

Прапори сортування, що використовуються різними функціями:

**`SORT_REGULAR`** (int)

**`SORT_REGULAR`** використовується для порівняння елементів масиву.

**`SORT_NUMERIC`** (int)

**`SORT_NUMERIC`** використовується для порівняння елементів як цифр.

**`SORT_STRING`** (int)

**`SORT_STRING`** використовується для порівняння елементів як рядків.

**`SORT_LOCALE_STRING`** (int)

**`SORT_LOCALE_STRING`** використовується для порівняння елементів як рядків на основі поточної локалі.

**`SORT_NATURAL`** (int)

**`SORT_NATURAL`** використовується для порівняння елементів як рядків, використовуючи природне впорядкування, таке як [natsort()](function.natsort.md)

**`SORT_FLAG_CASE`** (int)

**`SORT_FLAG_CASE`** може бути об'єднана (побітове АБО) з **`SORT_STRING`** або **`SORT_NATURAL`** для реєстронезалежного сортування рядків.

Опції фільтрації:

**`ARRAY_FILTER_USE_KEY`** (int)

**`ARRAY_FILTER_USE_KEY`** використовується у [arrayfilter()](function.array-filter.md) передачі кожного ключа як першого аргументу в задану функцію.

**`ARRAY_FILTER_USE_BOTH`** (int)

**`ARRAY_FILTER_USE_BOTH`** використовується у [arrayfilter()](function.array-filter.md) для передачі та значення та ключа в задану функцію.

**`COUNT_NORMAL`** (int)

**`COUNT_RECURSIVE`** (int)

**`EXTR_OVERWRITE`** (int)

**`EXTR_SKIP`** (int)

**`EXTR_PREFIX_SAME`** (int)

**`EXTR_PREFIX_ALL`** (int)

**`EXTR_PREFIX_INVALID`** (int)

**`EXTR_PREFIX_IF_EXISTS`** (int)

**`EXTR_IF_EXISTS`** (int)

**`EXTR_REFS`** (int)

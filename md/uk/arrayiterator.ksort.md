---
navigation:
  - arrayiterator.key.html: '« ArrayIterator::key'
  - arrayiterator.natcasesort.html: 'ArrayIterator::natcasesort »'
  - index.html: PHP Manual
  - class.arrayiterator.html: ArrayIterator
title: 'ArrayIterator::ksort'
---
# ArrayIterator::ksort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::ksort — Сортує елементи за ключами

### Опис

```methodsynopsis
public ArrayIterator::ksort(int $flags = SORT_REGULAR): bool
```

Сортує елементи за ключами.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

`flags`

Необов'язковий другий параметр `flags` може використовуватися для зміни поведінки сортування з використанням таких значень:

Прапори типу сортування:

-   **`SORT_REGULAR`** - Звичайне порівняння елементів; подробиці описані в розділі [оператори порівняння](language.operators.comparison.html)
-   **`SORT_NUMERIC`** - числове порівняння елементів
-   **`SORT_STRING`** - рядкове порівняння елементів
-   **`SORT_LOCALE_STRING`** - Порівняння елементів як рядки на основі поточного мовного стандарту. Використовується мовний стандарт, який можна змінити за допомогою [setlocale()](function.setlocale.html)
-   **`SORT_NATURAL`** - порівняння елементів як рядки, використовуючи "природний порядок", наприклад [natsort()](function.natsort.html)
-   **`SORT_FLAG_CASE`** - можна об'єднувати (побітове АБО) з **`SORT_STRING`** або **`SORT_NATURAL`** для сортування рядків без урахування регістру

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [ArrayIterator::asort()](arrayiterator.asort.html) - Сортує елементи за значеннями
-   [ArrayIterator::natcasesort()](arrayiterator.natcasesort.html) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort()](arrayiterator.natsort.html) - Сортує елементи "натурально"
-   [ArrayIterator::uasort()](arrayiterator.uasort.html) - Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.html) - Сортування за ключами за допомогою заданої функції порівняння
-   [ksort()](function.ksort.html) - Сортує масив за ключом у порядку зростання

---
navigation:
  - arrayiterator.append.md: '« ArrayIterator::append'
  - arrayiterator.construct.md: 'ArrayIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::asort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayIterator::asort

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ArrayIterator::asort — Сортує елементи за значеннями

### Опис

```methodsynopsis
public ArrayIterator::asort(int $flags = SORT_REGULAR): true
```

Сортує елементи за значеннями.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

`flags`

Необов'язковий другий параметр `flags` змінює поведінку сортування і може набувати таких значень:

Прапори типів сортування:

-   \*\*`SORT_REGULAR`\*\*- Звичайне порівняння елементів; подробиці описані в розділі[оператори порівняння](language.operators.comparison.md)
-   \*\*`SORT_NUMERIC`\*\*- Чисельне порівняння елементів
-   \*\*`SORT_STRING`\*\*- рядкове порівняння елементів
-   \*\*`SORT_LOCALE_STRING`\*\*— Порівняти елементи як рядки на основі поточного мовного стандарту. Прапор використовує мовний стандарт, який можна змінити функцією[setlocale()](function.setlocale.md)
-   **`SORT_NATURAL`** - Порівняння елементів як рядки, використовуючи "природний порядок", наприклад [natsort()](function.natsort.md)
-   \*\*`SORT_FLAG_CASE`**\- можна об'єднувати (побітове АБО) з**`SORT_STRING`** або **`SORT_NATURAL`\*\*для сортування рядків без урахування регістру

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Дивіться також

-   [ArrayIterator::ksort()](arrayiterator.ksort.md) \- Сортує елементи за ключами
-   [ArrayIterator::natcasesort()](arrayiterator.natcasesort.md) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort()](arrayiterator.natsort.md) - Сортує елементи "натурально"
-   [ArrayIterator::uasort()](arrayiterator.uasort.md) \- Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.md) \- Сортування за ключами за допомогою заданої функції порівняння
-   [asort()](function.asort.md) \- Сортує масив у порядку зростання, зберігаючи асоціацію індексів

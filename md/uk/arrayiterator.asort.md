Сортує елементи за значеннями

-   [« ArrayIterator::append](arrayiterator.append.md)
    
-   [ArrayIterator::construct »](arrayiterator.construct.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayIterator](class.arrayiterator.md)
    
-   Сортує елементи за значеннями
    

# ArrayIterator::asort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::asort — Сортує елементи за значеннями

### Опис

```methodsynopsis
public ArrayIterator::asort(int $flags = SORT_REGULAR): bool
```

Сортує елементи за значеннями.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

`flags`

Необов'язковий другий параметр `flags` може використовуватися для зміни поведінки сортування з використанням таких значень:

Прапори типу сортування:

-   **`SORT_REGULAR`** - Звичайне порівняння елементів; подробиці описані в розділі [оператори порівняння](language.operators.comparison.md)
-   **`SORT_NUMERIC`** - числове порівняння елементів
-   **`SORT_STRING`** - рядкове порівняння елементів
-   **`SORT_LOCALE_STRING`** - Порівняння елементів як рядки на основі поточного мовного стандарту. Використовується мовний стандарт, який можна змінити за допомогою [setlocale()](function.setlocale.md)
-   **`SORT_NATURAL`** - порівняння елементів як рядки, використовуючи "природний порядок", наприклад [natsort()](function.natsort.md)
-   **`SORT_FLAG_CASE`** - можна об'єднувати (побітове АБО) з **`SORT_STRING`** або **`SORT_NATURAL`** для сортування рядків без урахування регістру

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [ArrayIterator::ksort()](arrayiterator.ksort.md) - Сортує елементи за ключами
-   [ArrayIterator::natcasesort()](arrayiterator.natcasesort.md) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort()](arrayiterator.natsort.md) - Сортує елементи "натурально"
-   [ArrayIterator::uasort()](arrayiterator.uasort.md) - Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.md) - Сортування за ключами за допомогою заданої функції порівняння
-   [asort()](function.asort.md) - Сортує масив у порядку зростання та підтримує асоціацію індексів
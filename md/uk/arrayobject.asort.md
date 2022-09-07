---
navigation:
  - arrayobject.append.md: '« ArrayObject::append'
  - arrayobject.construct.md: 'ArrayObject::construct »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::asort'
---
# ArrayObject::asort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayObject::asort — Сортувати записи за значенням

### Опис

```methodsynopsis
public ArrayObject::asort(int $flags = SORT_REGULAR): bool
```

Сортує елементи масиву в порядку зростання, тому його ключі зберігають свою кореляцію зі значеннями, з якими вони пов'язані.

Використовується в основному при сортуванні асоціативних масивів, де важливим є фактичний порядок елементів.

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

### Приклади

**Приклад #1 Приклад використання **ArrayObject::asort()****

```php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
$fruitArrayObject = new ArrayObject($fruits);
$fruitArrayObject->asort();

foreach ($fruitArrayObject as $key => $val) {
    echo "$key = $val\n";
}
?>
```

Результат виконання цього прикладу:

```
c = apple
b = banana
d = lemon
a = orange
```

Назви фруктів були відсортовані за абеткою, і ключ, пов'язаний з кожним записом, був збережений.

### Дивіться також

-   [ArrayObject::ksort()](arrayobject.ksort.md) - Сортувати записи за ключами
-   [ArrayObject::natsort()](arrayobject.natsort.md) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::natcasesort()](arrayobject.natcasesort.md) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::uasort()](arrayobject.uasort.md) - Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort()](arrayobject.uksort.md) - Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [asort()](function.asort.md) - Сортує масив у порядку зростання та підтримує асоціацію індексів

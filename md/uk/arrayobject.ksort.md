---
navigation:
  - arrayobject.getiteratorclass.md: '« ArrayObject::getIteratorClass'
  - arrayobject.natcasesort.md: 'ArrayObject::natcasesort »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::ksort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::ksort

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ArrayObject::ksort — Сортувати записи за ключами

### Опис

```methodsynopsis
public ArrayObject::ksort(int $flags = SORT_REGULAR): true
```

Сортує масив за ключами, зберігаючи відносини між ключами та значеннями. Це корисно здебільшого до роботи з асоціативними масивами.

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

### Приклади

**Приклад #1 Приклад використання** ArrayObject::ksort()\*\*\*\*

```php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
$fruitArrayObject = new ArrayObject($fruits);
$fruitArrayObject->ksort();

foreach ($fruitArrayObject as $key => $val) {
    echo "$key = $val\n";
}
 ?>
```

Результат виконання наведеного прикладу:

```
a = orange
b = banana
c = apple
d = lemon
```

### Дивіться також

-   [ArrayObject::asort()](arrayobject.asort.md) \- Сортувати записи за значенням
-   [ArrayObject::natsort()](arrayobject.natsort.md) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::natcasesort()](arrayobject.natcasesort.md) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::uasort()](arrayobject.uasort.md) \- Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort()](arrayobject.uksort.md) \- Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [ksort()](function.ksort.md) \- Сортує масив за ключом у порядку зростання

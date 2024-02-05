---
navigation:
  - arrayobject.natcasesort.md: '« ArrayObject::natcasesort'
  - arrayobject.offsetexists.md: 'ArrayObject::offsetExists »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::natsort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::natsort

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

ArrayObject::natsort — Сортувати масив за допомогою алгоритму "natural order"

### Опис

```methodsynopsis
public ArrayObject::natsort(): true
```

Цей метод реалізує алгоритм сортування, при якому порядок літерно-цифрових рядків буде звичним для людини, зберігаючи при цьому ключ/значення. Такий алгоритм називається "природний порядок" (natural ordering). Приклад різниці між цим алгоритмом та звичайними алгоритмами сортування, (використовуються в [ArrayObject::asort](arrayobject.asort.md)) можна побачити у прикладі нижче.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Пример #1 Пример использования**ArrayObject::natsort()\*\*\*\*

```php
<?php
$array = array("img12.png", "img10.png", "img2.png", "img1.png");

$arr1 = new ArrayObject($array);
$arr2 = clone $arr1;

$arr1->asort();
echo "Стандартная сортировка\n";
print_r($arr1);

$arr2->natsort();
echo "\nСортировка в естественном порядке\n";
print_r($arr2);
?>
```

Результат виконання наведеного прикладу:

```
Стандартная сортировка
ArrayObject Object
(
    [3] => img1.png
    [1] => img10.png
    [0] => img12.png
    [2] => img2.png
)

Сортировка в естественном порядке
ArrayObject Object
(
    [3] => img1.png
    [2] => img2.png
    [1] => img10.png
    [0] => img12.png
)
```

Для більш детальної інформації дивіться сторінку Мартіна Пула (Martin Pool) [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Дивіться також

-   [ArrayObject::asort()](arrayobject.asort.md) \- Сортувати записи за значенням
-   [ArrayObject::ksort()](arrayobject.ksort.md) \- Сортувати записи за ключами
-   [ArrayObject::natcasesort()](arrayobject.natcasesort.md) - Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
-   [ArrayObject::uasort()](arrayobject.uasort.md) \- Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort()](arrayobject.uksort.md) \- Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [natsort()](function.natsort.md) - Сортує масив, використовуючи алгоритм "natural order"

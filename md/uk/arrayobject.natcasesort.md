Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"

-   [« ArrayObject::ksort](arrayobject.ksort.html)
    
-   [ArrayObject::natsort »](arrayobject.natsort.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"
    

# ArrayObject::natcasesort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayObject::natcasesort — Сортувати масив, використовуючи реєстронезалежний алгоритм "natural order"

### Опис

```methodsynopsis
public ArrayObject::natcasesort(): bool
```

Цей метод є реєстронезалежною версією [ArrayObject::natsort](arrayobject.natsort.html)

Цей метод реалізує алгоритм сортування, при якому порядок літерно-цифрових рядків буде звичним для людини, зберігаючи при цьому ключ/значення. Такий алгоритм називається "природний порядок" (natural ordering).

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::natcasesort()****

```php
<?php
$array = array('IMG0.png', 'img12.png', 'img10.png', 'img2.png', 'img1.png', 'IMG3.png');

$arr1 = new ArrayObject($array);
$arr2 = clone $arr1;

$arr1->asort();
echo "Стандартная сортировка\n";
print_r($arr1);

$arr2->natcasesort();
echo "\nСортировка в естественном порядке (без учёта регистра)\n";
print_r($arr2);
?>
```

Результат виконання цього прикладу:

```
Стандартная сортировка
ArrayObject Object
(
    [0] => IMG0.png
    [5] => IMG3.png
    [4] => img1.png
    [2] => img10.png
    [1] => img12.png
    [3] => img2.png
)

Сортировка в естественном порядке (без учёта регистра)
ArrayObject Object
(
    [0] => IMG0.png
    [4] => img1.png
    [3] => img2.png
    [5] => IMG3.png
    [2] => img10.png
    [1] => img12.png
)
```

Для більш детальної інформації дивіться сторінку Мартіна Пула (Martin Pool) [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Дивіться також

-   [ArrayObject::asort()](arrayobject.asort.html) - Сортувати записи за значенням
-   [ArrayObject::ksort()](arrayobject.ksort.html) - Сортувати записи за ключами
-   [ArrayObject::natsort()](arrayobject.natsort.html) - Сортувати масив, використовуючи алгоритм "natural order"
-   [ArrayObject::uasort()](arrayobject.uasort.html) - Сортувати записи, використовуючи функцію користувача для порівняння елементів і зберігаючи при цьому зв'язок ключ/значення
-   [ArrayObject::uksort()](arrayobject.uksort.html) - Сортувати масив за ключами, використовуючи функцію користувача для порівняння
-   [natcasesort()](function.natcasesort.html) - Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів
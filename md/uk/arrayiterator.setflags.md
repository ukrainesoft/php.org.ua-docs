Встановлює прапори, що змінюють поведінку.

-   [« ArrayIterator::serialize](arrayiterator.serialize.md)
    
-   [ArrayIterator::uasort »](arrayiterator.uasort.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayIterator](class.arrayiterator.md)
    
-   Встановлює прапори, що змінюють поведінку.
    

# ArrayIterator::setFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ArrayIterator::setFlags — Встановлює прапори, що змінюють поведінку ArrayIterator

### Опис

```methodsynopsis
public ArrayIterator::setFlags(int $flags): void
```

Встановлює прапори, які керують поведінкою.

### Список параметрів

`flags`

Поведінка нового ArrayIterator. Приймає або бітову маску, або названі константи. Використання іменованих констант рекомендується для забезпечення сумісності з майбутніми версіями.

Доступні прапори поведінки наведені нижче. Фактичний зміст цих прапорів описаний у [визначених константах](class.arrayiterator.html#arrayiterator.constants)

**Прапори поведінки ArrayIterator**

| значение | константа                                                                                      |
|----------|------------------------------------------------------------------------------------------------|
|          | [ArrayIterator::STDPROPLIST](class.arrayiterator.html#arrayiterator.constants.std-prop-list)   |
|          | [ArrayIterator::ARRAYАСPROPS](class.arrayiterator.html#arrayiterator.constants.array-as-props) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ArrayIterator::getFlags()](arrayiterator.getflags.md) - Отримує прапори поведінки
Встановлює прапори, що змінюють поведінку.

-   [« ArrayIterator::serialize](arrayiterator.serialize.html)
    
-   [ArrayIterator::uasort »](arrayiterator.uasort.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayIterator](class.arrayiterator.html)
    
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

Доступні прапори поведінки наведені нижче. Фактичний зміст цих прапорів описаний у [предопределённых константах](class.arrayiterator.html#arrayiterator.constants)

**Прапори поведінки ArrayIterator**

| значение | константа |
| --- | --- |
|  | [ArrayIterator::STD\_PROP\_LIST](class.arrayiterator.html#arrayiterator.constants.std-prop-list) |
|  | [ArrayIterator::ARRAY\_AS\_PROPS](class.arrayiterator.html#arrayiterator.constants.array-as-props) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ArrayIterator::getFlags()](arrayiterator.getflags.html) - Отримує прапори поведінки
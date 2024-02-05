---
navigation:
  - arrayiterator.serialize.md: '« ArrayIterator::serialize'
  - arrayiterator.uasort.md: 'ArrayIterator::uasort »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayIterator::setFlags

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ArrayIterator::setFlags — Встановлює прапори, що змінюють поведінку ArrayIterator

### Опис

```methodsynopsis
public ArrayIterator::setFlags(int $flags): void
```

Встановлює прапори, які керують поведінкою.

### Список параметрів

`flags`

Поведінка нового ArrayIterator. Приймає або бітову маску, або названі константи. Використання іменованих констант рекомендується для забезпечення сумісності з майбутніми версіями.

Доступні прапори поведінки наведені нижче. Фактичний зміст цих прапорів описаний у [визначених константах](class.arrayiterator.md#arrayiterator.constants)

**Прапори поведінки ArrayIterator**

| значение | константа |
| --- | --- |
|  | [ArrayIterator::STD\_PROP\_LIST](class.arrayiterator.md#arrayiterator.constants.std-prop-list) |
|  | [ArrayIterator::ARRAY\_AS\_PROPS](class.arrayiterator.md#arrayiterator.constants.array-as-props) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ArrayIterator::getFlags()](arrayiterator.getflags.md) \- Отримує прапори поведінки

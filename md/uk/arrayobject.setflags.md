---
navigation:
  - arrayobject.serialize.md: '« ArrayObject::serialize'
  - arrayobject.setiteratorclass.md: 'ArrayObject::setIteratorClass »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::setFlags

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ArrayObject::setFlags — Встановлює прапори поведінки

### Опис

```methodsynopsis
public ArrayObject::setFlags(int $flags): void
```

Встановлює прапори, які впливають на поведінку ArrayObject.

### Список параметрів

`flags`

Нова поведінка ArrayObject. Допускається або бітова маска, або названі константи. Використання іменованих констант рекомендується для забезпечення сумісності з майбутніми версіями.

Доступні прапори поведінки наведені нижче. Фактичні значення цих прапорів описані у розділі [зумовлені константи](class.arrayobject.md#arrayobject.constants)

**Прапори поведінки ArrayObject**

| Значение | Константа |
| --- | --- |
|  | [ArrayObject::STD\_PROP\_LIST](class.arrayobject.md#arrayobject.constants.std-prop-list) |
|  | [ArrayObject::ARRAY\_AS\_PROPS](class.arrayobject.md#arrayobject.constants.array-as-props) |

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ArrayObject::setFlags()\*\*\*\*

```php
<?php
// Массив с доступными фруктами
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Попытка использовать ключ массива как свойство
var_dump($fruitsArrayObject->lemons);
// Установка флага, позволяющего использовать ключи массива как свойства ArrayObject
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);
// Новая попытка
var_dump($fruitsArrayObject->lemons);
?>
```

Результат виконання наведеного прикладу:

```
NULL
int(1)
```

---
navigation:
  - arrayobject.getarraycopy.md: '« ArrayObject::getArrayCopy'
  - arrayobject.getiterator.md: 'ArrayObject::getIterator »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::getFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::getFlags

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ArrayObject::getFlags — Отримує прапори поведінки

### Опис

```methodsynopsis
public ArrayObject::getFlags(): int
```

Получает флаги поведения[ArrayObject](class.arrayobject.md)Смотрите метод[ArrayObject::setFlags](arrayobject.setflags.md) Щоб переглянути список можливих прапорів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає прапори поведінки ArrayObject.

### Приклади

**Пример #1 Пример использования**ArrayObject::getFlags()\*\*\*\*

```php
<?php
// Массив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Получение текущих флагов
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);

// Установка новых флагов
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);

// Получение новых флагов
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);
?>
```

Результат виконання наведеного прикладу:

```
int(0)
int(2)
```

### Дивіться також

-   Метод[ArrayObject::setFlags()](arrayobject.setflags.md) \- Встановлює прапори поведінки

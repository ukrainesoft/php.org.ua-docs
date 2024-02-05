---
navigation:
  - weakreference.get.md: '« WeakReference::get'
  - weakmap.count.md: 'WeakMap::count »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас WeakMap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас WeakMap

(PHP 8)

## Вступ

**WeakMap** - це колекція (map) або словник, який приймає об'єкти як ключі. Однак, на відміну від аналогічного в іншому [SplObjectStorage](class.splobjectstorage.md), об'єкт у ключі **WeakMap** не впливає на лічильник посилань об'єкта. Тобто, якщо в якийсь момент єдиним посиланням на об'єкт є ключ **WeakMap**, об'єкт буде зібраний збирачем сміття та видалено з **WeakMap**. Його основний варіант використання – створення кешів даних, отриманих з об'єкта, яким не потрібно жити довше, ніж об'єкт.

**WeakMap** реалізує [ArrayAccess](class.arrayaccess.md) [Iterator](class.iterator.md) і [Countable](class.countable.md)Тому у більшості випадків його можна використовувати так само, як асоціативний масив.

## Огляд класів

```classsynopsis

    
     final
     class WeakMap
    

    
     implements
      ArrayAccess,

     Countable,

     IteratorAggregate {

    /* Методы */
    
   public count(): int
public getIterator(): Iterator
public offsetExists(object $object): bool
public offsetGet(object $object): mixed
public offsetSet(object $object, mixed $value): void
public offsetUnset(object $object): void

   }
```

## Приклади

**Приклад #1 Приклад використання** Weakmap\*\*\*\*

```php
<?php
$wm = new WeakMap();

$o = new stdClass;

class A {
    public function __destruct() {
        echo "Уничтожено!\n";
    }
}

$wm[$o] = new A;

var_dump(count($wm));
echo "Сброс...\n";
unset($o);
echo "Готово\n";
var_dump(count($wm));
```

Результат виконання наведеного прикладу:

```
int(1)
Сброс...
Уничтожено!
Готово
int(0)
```

## Зміст

-   [WeakMap::count](weakmap.count.md)— Підраховує кількість живих записів у колекції (map)
-   [WeakMap::getIterator](weakmap.getiterator.md)— Отримує зовнішній ітератор
-   [WeakMap::offsetExists](weakmap.offsetexists.md)— Перевіряє, чи є у колекції (map) певний об'єкт
-   [WeakMap::offsetGet](weakmap.offsetget.md)— Повертає значення, на яке вказує певний об'єкт
-   [WeakMap::offsetSet](weakmap.offsetset.md)— Оновлює колекцію (map) новою парою ключ-значення
-   [WeakMap::offsetUnset](weakmap.offsetunset.md)— Видаляє запис із колекції (map)

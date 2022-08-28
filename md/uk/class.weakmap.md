Клас WeakMap

-   [« WeakReference::get](weakreference.get.html)
    
-   [WeakMap::\_\_construct »](ext-weakmap.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Встроенные интерфейсы и классы](reserved.interfaces.html)
    
-   Клас WeakMap
    

# Клас WeakMap

(PHP 8)

## Вступ

**WeakMap** - це колекція (map) або словник, який приймає об'єкти як ключі. Однак, на відміну від аналогічного в іншому [SplObjectStorage](class.splobjectstorage.html), об'єкт у ключі **WeakMap** не впливає на лічильник посилань об'єкта. Тобто, якщо в якийсь момент єдиним посиланням на об'єкт є ключ **WeakMap**, об'єкт буде зібраний збирачем сміття та видалено з **WeakMap**. Його основний варіант використання – створення кешів даних, отриманих з об'єкта, яким не потрібно жити довше, ніж об'єкт.

**WeakMap** реалізує [ArrayAccess](class.arrayaccess.html) [Iterator](class.iterator.html) і [Countable](class.countable.html)Тому у більшості випадків його можна використовувати так само, як асоціативний масив.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class WeakMap
     

     implements 
       ArrayAccess,  Countable,  IteratorAggregate {

    /* Методы */
    
   public __construct()

    public count(): int
public getIterator(): Iterator
public offsetExists(object $object): bool
public offsetGet(object $object): mixed
public offsetSet(object $object, mixed $value): void
public offsetUnset(object $object): void

   }
```

## Приклади

**Приклад #1 Приклад використання **Weakmap****

```php
<?php
$wm = new WeakMap();

$o = new StdClass;

class A {
    public function __destruct() {
        echo "Уничтожено!\n";
    }
}

$wm[$o] = new A;

var_dump(count($wm));
echo "Сброс...\n";
unset($o);
echo "Готово\n";
var_dump(count($wm));
```

Результат виконання цього прикладу:

```
int(1)
Сброс...
Уничтожено!
Готово
int(0)
```

## Зміст

-   [WeakMap::\_\_construct](ext-weakmap.construct.html) - Створює нову колекцію (map)
-   [WeakMap::count](weakmap.count.html) — Підраховує кількість живих записів у колекції (map)
-   [WeakMap::getIterator](weakmap.getiterator.html) — Отримує зовнішній ітератор
-   [WeakMap::offsetExists](weakmap.offsetexists.html) — Перевіряє, чи є у колекції (map) певний об'єкт
-   [WeakMap::offsetGet](weakmap.offsetget.html) — Повертає значення, на яке вказує певний об'єкт
-   [WeakMap::offsetSet](weakmap.offsetset.html) - Оновлює колекцію (map) новою парою ключ-значення
-   [WeakMap::offsetUnset](weakmap.offsetunset.html) — Видаляє запис із колекції (map)
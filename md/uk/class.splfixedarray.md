---
navigation:
  - splpriorityqueue.valid.md: '« SplPriorityQueue::valid'
  - splfixedarray.construct.md: 'SplFixedArray::\_\_construct »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplFixedArray
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplFixedArray

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplFixedArray забезпечує базову функціональність, що надається масивами. Головна різниця між SplFixedArray та звичайним масивом PHP у тому, що розмір SplFixedArray необхідно змінювати вручну, а як індекси можуть виступати лише цілочисельні значення. Перевага цих обмежень полягає у меншому використанні пам'яті, ніж стандартний масив (array).

## Огляд класів

```classsynopsis

    
     class SplFixedArray
    

    
     implements
      IteratorAggregate,

     ArrayAccess,

     Countable,

     JsonSerializable {

    /* Методы */
    
   public __construct(int $size = 0)

    public count(): int
public current(): mixed
public static fromArray(array $array, bool $preserveKeys = true): SplFixedArray
public getIterator(): Iterator
public getSize(): int
public jsonSerialize(): mixed
public key(): int
public next(): void
public offsetExists(int $index): bool
public offsetGet(int $index): mixed
public offsetSet(int $index, mixed $value): void
public offsetUnset(int $index): void
public rewind(): void
public __serialize(): array
public setSize(int $size): bool
public toArray(): array
public __unserialize(array $data): void
public valid(): bool
public __wakeup(): void

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Магічні методи[SplFixedArray::\_\_serialize()](splfixedarray.serialize.md) і [SplFixedArray::\_\_unserialize()](splfixedarray.unserialize.md) додані в **SplFixedArray** |
| 8.1.0 | Класс**SplFixedArray** тепер реалізує інтерфейс [JsonSerializable](class.jsonserializable.md) |
| 8.0.0 | Класс**SplFixedArray** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше було реалізовано інтерфейс [Iterator](class.iterator.md) |

## Приклади

**Приклад #1 Приклад використання** SplFixedArray\*\*\*\*

```php
<?php
// Инициализация массива фиксированной длиной
$array = new SplFixedArray(5);

$array[1] = 2;
$array[4] = "foo";

var_dump($array[0]); // NULL
var_dump($array[1]); // int(2)

var_dump($array["4"]); // string(3) "foo"

// Увеличение размера массива до 10
$array->setSize(10);

$array[9] = "asdf";

// Сокращаем размер массива до 2-х
$array->setSize(2);

// Следующий код вызывает исключение RuntimeException: Index invalid or out of range
try {
    var_dump($array["non-numeric"]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}

try {
    var_dump($array[-1]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}

try {
    var_dump($array[5]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}
?>
```

Результат виконання наведеного прикладу:

```
NULL
int(2)
string(3) "foo"
RuntimeException: Index invalid or out of range
RuntimeException: Index invalid or out of range
RuntimeException: Index invalid or out of range
```

## Зміст

-   [SplFixedArray::\_\_construct](splfixedarray.construct.md) \- Створює новий масив фіксованої довжини
-   [SplFixedArray::count](splfixedarray.count.md)— Повертає розмір масиву
-   [SplFixedArray::current](splfixedarray.current.md)— Повертає поточний елемент масиву
-   [SplFixedArray::fromArray](splfixedarray.fromarray.md) \- Імпортує PHP-масив в об'єкт класу SplFixedArray
-   [SplFixedArray::getIterator](splfixedarray.getiterator.md)— Отримує ітератор для переходу масивом
-   [SplFixedArray::getSize](splfixedarray.getsize.md)— Отримує розмір масиву
-   [SplFixedArray::jsonSerialize](splfixedarray.jsonserialize.md)— Повертає виставу, яка може бути перетворена на JSON
-   [SplFixedArray::key](splfixedarray.key.md)— Повертає індекс поточного елемента масиву
-   [SplFixedArray::next](splfixedarray.next.md)— Переходить до наступного елементу масиву
-   [SplFixedArray::offsetExists](splfixedarray.offsetexists.md)— Повертає факт наявності зазначеного індексу масиву
-   [SplFixedArray::offsetGet](splfixedarray.offsetget.md)— Повертає значення за вказаним індексом
-   [SplFixedArray::offsetSet](splfixedarray.offsetset.md)— Встановлює нове значення за заданим індексом
-   [SplFixedArray::offsetUnset](splfixedarray.offsetunset.md)— Видаляє значення за індексом $index
-   [SplFixedArray::rewind](splfixedarray.rewind.md) \- Встановлює ітератор масиву на початок
-   [SplFixedArray::\_\_serialize](splfixedarray.serialize.md)— Серіалізує об'єкт SplFixedArray
-   [SplFixedArray::setSize](splfixedarray.setsize.md) \- Змінює розмір масиву
-   [SplFixedArray::toArray](splfixedarray.toarray.md) \- Повертає звичайний PHP-масив зі значеннями фіксованого масиву
-   [SplFixedArray::\_\_unserialize](splfixedarray.unserialize.md)— Десеріалізує параметр data в об'єкті SplFixedArray
-   [SplFixedArray::valid](splfixedarray.valid.md) \- Перевіряє масив на наявність елементів
-   [SplFixedArray::\_\_wakeup](splfixedarray.wakeup.md) \- Переініціалізація масиву після десеріалізації

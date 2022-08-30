Клас SplFixedArray

-   [« SplPriorityQueue::valid](splpriorityqueue.valid.html)
    
-   [SplFixedArray::construct »](splfixedarray.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Структури даних](spl.datastructures.html)
    
-   Клас SplFixedArray
    

# Клас SplFixedArray

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplFixedArray забезпечує базову функціональність, що надається масивами. Головна різниця між SplFixedArray і звичайним масивом PHP у тому, що розмір SplFixedArray необхідно змінювати вручну, а як індекси можуть виступати тільки цілі значення. Перевага цих обмежень полягає у меншому використанні пам'яті, ніж стандартний масив (array).

## Огляд класів

```classsynopsis

     
    

    
     
      class SplFixedArray
     

     implements 
       IteratorAggregate,  ArrayAccess,  Countable,  JsonSerializable {

    /* Методы */
    
   public __construct(int $size = 0)

    public count(): int
public current(): mixed
public static fromArray(array $array, bool $preserveKeys = true): SplFixedArray
public getSize(): int
public key(): int
public next(): void
public offsetExists(int $index): bool
public offsetGet(int $index): mixed
public offsetSet(int $index, mixed $value): void
public offsetUnset(int $index): void
public rewind(): void
public setSize(int $size): bool
public toArray(): array
public valid(): bool
public __wakeup(): void

   }
```

## список змін

| Версия | Описание                                                                                                                                                             |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Клас **SplFixedArray** тепер реалізує інтерфейс [JsonSerializable](class.jsonserializable.html)                                                                      |
|        | Клас **SplFixedArray** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше було реалізовано інтерфейс [Iterator](class.iterator.html) |

## Приклади

**Приклад #1 Приклад використання **SplFixedArray****

```php
<?php
// Инициализация массива фиксированной длиной
$array = new SplFixedArray(5);

$array[1] = 2;
$array[4] = "foo";

var_dump($array[0]); // NULL
var_dump($array[1]); // int(2)

var_dump($array["4"]); // string(3) "foo"

// Увеличение размера массива до 10
$array->setSize(10);

$array[9] = "asdf";

// Сокращаем размер массива до 2-х
$array->setSize(2);

// Следующий код вызывает исключение RuntimeException: Index invalid or out of range
try {
    var_dump($array["non-numeric"]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}

try {
    var_dump($array[-1]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}

try {
    var_dump($array[5]);
} catch(RuntimeException $re) {
    echo "RuntimeException: ".$re->getMessage()."\n";
}
?>
```

Результат виконання цього прикладу:

```
NULL
int(2)
string(3) "foo"
RuntimeException: Index invalid or out of range
RuntimeException: Index invalid or out of range
RuntimeException: Index invalid or out of range
```

## Зміст

-   [SplFixedArray::construct](splfixedarray.construct.html) - Створює новий масив фіксованої довжини
-   [SplFixedArray::count](splfixedarray.count.html) — Повертає розмір масиву
-   [SplFixedArray::current](splfixedarray.current.html) — Повертає поточний елемент масиву
-   [SplFixedArray::fromArray](splfixedarray.fromarray.html) - Імпортує PHP-масив в об'єкт класу SplFixedArray
-   [SplFixedArray::getSize](splfixedarray.getsize.html) — Отримує розмір масиву
-   [SplFixedArray::key](splfixedarray.key.html) — Повертає індекс поточного елемента масиву
-   [SplFixedArray::next](splfixedarray.next.html) — Переходить до наступного елементу масиву
-   [SplFixedArray::offsetExists](splfixedarray.offsetexists.html) — Повертає факт наявності зазначеного індексу масиву
-   [SplFixedArray::offsetGet](splfixedarray.offsetget.html) — Повертає значення за вказаним індексом
-   [SplFixedArray::offsetSet](splfixedarray.offsetset.html) — Встановлює нове значення за заданим індексом
-   [SplFixedArray::offsetUnset](splfixedarray.offsetunset.html) — Видаляє значення за індексом $index
-   [SplFixedArray::rewind](splfixedarray.rewind.html) - Встановлює ітератор масиву на початок
-   [SplFixedArray::setSize](splfixedarray.setsize.html) - Змінює розмір масиву
-   [SplFixedArray::toArray](splfixedarray.toarray.html) - Повертає звичайний PHP-масив зі значеннями фіксованого масиву
-   [SplFixedArray::valid](splfixedarray.valid.html) - Перевіряє масив на наявність елементів
-   [SplFixedArray::wakeup](splfixedarray.wakeup.html) - Переініціалізація масиву після десеріалізації
Клас Set

-   [« DsPair::toArray](ds-pair.toarray.html)
    
-   [ДсSet::add »](ds-set.add.html)
    
-   [PHP Manual](index.md)
    
-   [Структури даних](book.ds.md)
    
-   Клас Set
    

# Клас Set

(No version information available, might only be in Git)

## Вступ

Set – це послідовність унікальних значень. Реалізація використовує ту ж хеш-таблицю, що й **ДсMap**, В якій значення використовуються як ключі, а зв'язані значення ігноруються.

## Сильні сторони

-   Значення можуть бути будь-якого типу, включаючи об'єкти.
-   Підтримує синтаксис масиву (квадратні дужки).
-   Зберігається порядок вставки.
-   Автоматично звільняє пам'ять, коли кількість елементів значно зменшується.
-   **add()** **remove()** і **contains()** мають складність O(1).

## Слабкі сторони

-   Не підтримує **push()** **pop()** **insert()** **shift()** і **unshift()**
-   **get()** має складність O(n), якщо є віддалені значення буфері, до значення, до якого відбувається доступ. Інакше O(1).

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Set
     

     implements 
       Ds\Collection,  ArrayAccess {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 16;


    /* Методы */
    
   public add(mixed ...$values): void
public allocate(int $capacity): void
public capacity(): int
public clear(): void
public contains(mixed ...$values): bool
public copy(): Ds\Set
public diff(Ds\Set $set): Ds\Set
public filter(callable $callback = ?): Ds\Set
public first(): mixed
public get(int $index): mixed
public intersect(Ds\Set $set): Ds\Set
public isEmpty(): bool
public join(string $glue = ?): string
public last(): mixed
public merge(mixed $values): Ds\Set
public reduce(callable $callback, mixed $initial = ?): mixed
public remove(mixed ...$values): void
public reverse(): void
public reversed(): Ds\Set
public slice(int $index, int $length = ?): Ds\Set
public sort(callable $comparator = ?): void
public sorted(callable $comparator = ?): Ds\Set
public sum(): int|float
public toArray(): array
public union(Ds\Set $set): Ds\Set
public xor(Ds\Set $set): Ds\Set

   }
```

## Обумовлені константи

**`Ds\Set::MIN_CAPACITY`**

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсSet::add](ds-set.add.html) — Додає значення до набору
-   [ДсSet::allocate](ds-set.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [ДсSet::capacity](ds-set.capacity.html) — Повертає поточну місткість
-   [ДсSet::clear](ds-set.clear.html) — Видаляє всі значення з колекції
-   [ДсSet::construct](ds-set.construct.html) - Створює новий екземпляр класу
-   [ДсSet::contains](ds-set.contains.html) — Перевіряє, чи міститься в колекції задані значення
-   [ДсSet::copy](ds-set.copy.html) — Повертає поверхневу копію колекції
-   [ДсSet::count](ds-set.count.html) — Повертає кількість елементів колекції
-   [ДсSet::diff](ds-set.diff.html) — Створює новий набір із елементами, яких немає в іншому наборі
-   [ДсSet::filter](ds-set.filter.html) — Створює новий список із елементів, вибраних за допомогою заданої callback-функції
-   [ДсSet::first](ds-set.first.html) — Повертає перший елемент колекції
-   [ДсSet::get](ds-set.get.html) — Повертає значення за індексом
-   [ДсSet::intersect](ds-set.intersect.html) — Створює новий набір, створений перетином з іншим набором
-   [ДсSet::isEmpty](ds-set.isempty.html) — Перевіряє, чи колекція порожня.
-   [ДсSet::join](ds-set.join.html) — Склеює всі значення в рядок
-   [ДсSet::jsonSerialize](ds-set.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [ДсSet::last](ds-set.last.html) — Повертає останнє значення колекції
-   [ДсSet::merge](ds-set.merge.html) — Повертає результат додавання всіх заданих значень до набору
-   [ДсSet::reduce](ds-set.reduce.html) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [ДсSet::remove](ds-set.remove.html) — Видаляє всі задані значення набору
-   [ДсSet::reverse](ds-set.reverse.html) — Перевертає поточну колекцію
-   [ДсSet::reversed](ds-set.reversed.html) — Повертає перегорнуту копію колекції
-   [ДсSet::slice](ds-set.slice.html) — Повертає піднабір із заданого діапазону
-   [ДсSet::sort](ds-set.sort.html) — Сортує колекцію
-   [ДсSet::sorted](ds-set.sorted.html) — Повертає копію колекції, відсортовану за значенням.
-   [ДсSet::sum](ds-set.sum.html) — Повертає суму всіх значень колекції
-   [ДсSet::toArray](ds-set.toarray.html) — Перетворює колекцію на масив (array)
-   [ДсSet::union](ds-set.union.html) — Створює новий набір з елементів поточного та переданого наборів
-   [ДсSet::xor](ds-set.xor.html) — Створює новий набір із значень, які є в одному з наборів, але не в обох одночасно
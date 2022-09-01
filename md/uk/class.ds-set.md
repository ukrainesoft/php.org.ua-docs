---
navigation:
  - ds-pair.toarray.html: '« DsPair::toArray'
  - ds-set.add.html: 'ДсSet::add »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Set
---
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

-   [ДсSet::add](ds-set.add.md) — Додає значення до набору
-   [ДсSet::allocate](ds-set.allocate.md) — Виділяє пам'ять під зазначену місткість
-   [ДсSet::capacity](ds-set.capacity.md) — Повертає поточну місткість
-   [ДсSet::clear](ds-set.clear.md) — Видаляє всі значення з колекції
-   [ДсSet::construct](ds-set.construct.md) - Створює новий екземпляр класу
-   [ДсSet::contains](ds-set.contains.md) — Перевіряє, чи міститься в колекції задані значення
-   [ДсSet::copy](ds-set.copy.md) — Повертає поверхневу копію колекції
-   [ДсSet::count](ds-set.count.md) — Повертає кількість елементів колекції
-   [ДсSet::diff](ds-set.diff.md) — Створює новий набір із елементами, яких немає в іншому наборі
-   [ДсSet::filter](ds-set.filter.md) — Створює новий список із елементів, вибраних за допомогою заданої callback-функції
-   [ДсSet::first](ds-set.first.md) — Повертає перший елемент колекції
-   [ДсSet::get](ds-set.get.md) — Повертає значення за індексом
-   [ДсSet::intersect](ds-set.intersect.md) — Створює новий набір, створений перетином з іншим набором
-   [ДсSet::isEmpty](ds-set.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсSet::join](ds-set.join.md) — Склеює всі значення в рядок
-   [ДсSet::jsonSerialize](ds-set.jsonserialize.md) — Повертає колекцію в JSON-представництві
-   [ДсSet::last](ds-set.last.md) — Повертає останнє значення колекції
-   [ДсSet::merge](ds-set.merge.md) — Повертає результат додавання всіх заданих значень до набору
-   [ДсSet::reduce](ds-set.reduce.md) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [ДсSet::remove](ds-set.remove.md) — Видаляє всі задані значення набору
-   [ДсSet::reverse](ds-set.reverse.md) — Перевертає поточну колекцію
-   [ДсSet::reversed](ds-set.reversed.md) — Повертає перегорнуту копію колекції
-   [ДсSet::slice](ds-set.slice.md) — Повертає піднабір із заданого діапазону
-   [ДсSet::sort](ds-set.sort.md) — Сортує колекцію
-   [ДсSet::sorted](ds-set.sorted.md) — Повертає копію колекції, відсортовану за значенням.
-   [ДсSet::sum](ds-set.sum.md) — Повертає суму всіх значень колекції
-   [ДсSet::toArray](ds-set.toarray.md) — Перетворює колекцію на масив (array)
-   [ДсSet::union](ds-set.union.md) — Створює новий набір з елементів поточного та переданого наборів
-   [ДсSet::xor](ds-set.xor.md) — Створює новий набір із значень, які є в одному з наборів, але не в обох одночасно

---
navigation:
  - ds-hashable.hash.md: '« Ds\\Hashable::hash'
  - ds-sequence.allocate.md: 'Ds\\Sequence::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Інтерфейс Sequence
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Sequence

(PECL ds >= 1.0.0)

## Вступ

Послідовність описує поведінку, у якому значення розподілені у одному, лінійному порядку. У деяких мовах ця поведінка описується як "List". Це схоже на масив, в якому використовуються цілі ключі, за винятком декількох моментів:

-   Значення завжди проіндексовані по порядку\[0, 1, 2, …, size - 1\]
-   Можна звертатися лише до значень індексованих у діапазоні\[0, size - 1\]

У яких випадках використовується:

-   Якщо ви хочете використовувати масив як список (не звертаючи уваги на ключі).
-   Більш ефективна альтернатива для[SplDoublyLinkedList](class.spldoublylinkedlist.md) і [SplFixedArray](class.splfixedarray.md)

## Огляд інтерфейсів

```classsynopsis

    interface Ds\Sequence

    extends
      Ds\Collection,
     ArrayAccess {

    /* Методы */
    
   abstract public allocate(int $capacity): void
abstract public apply(callable $callback): void
abstract public capacity(): int
abstract public contains(mixed ...$values): bool
abstract public filter(callable $callback = ?): Ds\Sequence
abstract public find(mixed $value): mixed
abstract public first(): mixed
abstract public get(int $index): mixed
abstract public insert(int $index, mixed ...$values): void
abstract public join(string $glue = ?): string
abstract public last(): mixed
abstract public map(callable $callback): Ds\Sequence
abstract public merge(mixed $values): Ds\Sequence
abstract public pop(): mixed
abstract public push(mixed ...$values): void
abstract public reduce(callable $callback, mixed $initial = ?): mixed
abstract public remove(int $index): mixed
abstract public reverse(): void
abstract public reversed(): Ds\Sequence
abstract public rotate(int $rotations): void
abstract public set(int $index, mixed $value): void
abstract public shift(): mixed
abstract public slice(int $index, int $length = ?): Ds\Sequence
abstract public sort(callable $comparator = ?): void
abstract public sorted(callable $comparator = ?): Ds\Sequence
abstract public sum(): int|float
abstract public unshift(mixed $values = ?): void


    /* Наследуемые методы */
    public Ds\Collection::clear(): void
public Ds\Collection::copy(): Ds\Collection
public Ds\Collection::isEmpty(): bool
public Ds\Collection::toArray(): array

    public Countable::count(): int

    public IteratorAggregate::getIterator(): Traversable

    public JsonSerializable::jsonSerialize(): mixed

    public ArrayAccess::offsetExists(mixed $offset): bool
public ArrayAccess::offsetGet(mixed $offset): mixed
public ArrayAccess::offsetSet(mixed $offset, mixed $value): void
public ArrayAccess::offsetUnset(mixed $offset): void


   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [Ds\\Sequence::allocate](ds-sequence.allocate.md)— Виділення пам'яті під зазначену місткість
-   [Ds\\Sequence::apply](ds-sequence.apply.md)— Оновлення всіх значень застосуванням переданої callback-функції до них
-   [Ds\\Sequence::capacity](ds-sequence.capacity.md)— Повертає поточну місткість
-   [Ds\\Sequence::contains](ds-sequence.contains.md)— Перевіряє, чи містяться в колекції задані значення
-   [Ds\\Sequence::filter](ds-sequence.filter.md)— Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Sequence::find](ds-sequence.find.md) \- Пошук індексу за значенням
-   [Ds\\Sequence::first](ds-sequence.first.md)— Повертає перший елемент колекції
-   [Ds\\Sequence::get](ds-sequence.get.md)— Повертає значення за індексом
-   [Ds\\Sequence::insert](ds-sequence.insert.md)— Вставляє значення за вказаним індексом
-   [Ds\\Sequence::join](ds-sequence.join.md) \- Склеює всі значення в рядок
-   [Ds\\Sequence::last](ds-sequence.last.md)— Повертає останнє значення колекції
-   [Ds\\Sequence::map](ds-sequence.map.md)— Повертає результат застосування callback-функції до всіх значень колекції.
-   [Ds\\Sequence::merge](ds-sequence.merge.md)— Повертає результат додавання всіх заданих значень до колекції
-   [Ds\\Sequence::pop](ds-sequence.pop.md)— Видаляє та повертає останнє значення
-   [Ds\\Sequence::push](ds-sequence.push.md)— Додає значення до кінця послідовності
-   [Ds\\Sequence::reduce](ds-sequence.reduce.md) \- Сплескує колекцію до одного значення використовуючи callback-функцію
-   [Ds\\Sequence::remove](ds-sequence.remove.md)— Видаляє та повертає значення за індексом
-   [Ds\\Sequence::reverse](ds-sequence.reverse.md)— Перевертає поточну колекцію
-   [Ds\\Sequence::reversed](ds-sequence.reversed.md)— Повертає перегорнуту копію колекції
-   [Ds\\Sequence::rotate](ds-sequence.rotate.md)— Перемотує послідовність на задану кількість значень
-   [Ds\\Sequence::set](ds-sequence.set.md)— Замінює значення за вказаним індексом
-   [Ds\\Sequence::shift](ds-sequence.shift.md)— Видаляє та повертає перше значення
-   [Ds\\Sequence::slice](ds-sequence.slice.md)— Повертає під-колекцію із заданого діапазону
-   [Ds\\Sequence::sort](ds-sequence.sort.md)— Сортує колекцію
-   [Ds\\Sequence::sorted](ds-sequence.sorted.md)— Повертає копію колекції, відсортовану за значенням.
-   [Ds\\Sequence::sum](ds-sequence.sum.md)— Повертає суму всіх значень колекції
-   [Ds\\Sequence::unshift](ds-sequence.unshift.md)— Додає значення на початок послідовності

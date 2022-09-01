---
navigation:
  - ds-hashable.hash.html: '« DsHashable::hash'
  - ds-sequence.allocate.html: 'ДсSequence::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Інтерфейс Sequence
---
# Інтерфейс Sequence

(No version information available, might only be in Git)

## Вступ

Послідовність описує поведінку, у якому значення розподілені у одному, лінійному порядку. У деяких мовах ця поведінка описується як "List". Це схоже на масив, в якому використовуються цілі ключі, за винятком декількох моментів:

-   Значення завжди проіндексовані по порядку 0, 1, 2, …, size - 1
-   Можна звертатися лише до значень індексованих у діапазоні 0, size - 1

У яких випадках використовується:

-   Якщо ви хочете використовувати масив як список (не звертаючи уваги на ключі).
-   Більш ефективна альтернатива для [SplDoublyLinkedList](class.spldoublylinkedlist.md) і [SplFixedArray](class.splfixedarray.md)

## Огляд інтерфейсів

```classsynopsis


    
    

     class Ds\Sequence
     implements  Ds\Collection,  ArrayAccess {
    

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

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсSequence::allocate](ds-sequence.allocate.md) — Виділення пам'яті під зазначену місткість
-   [ДсSequence::apply](ds-sequence.apply.md) — Оновлення всіх значень застосуванням переданої callback-функції до них
-   [ДсSequence::capacity](ds-sequence.capacity.md) — Повертає поточну місткість
-   [ДсSequence::contains](ds-sequence.contains.md) — Перевіряє, чи містяться в колекції задані значення
-   [ДсSequence::filter](ds-sequence.filter.md) — Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції
-   [ДсSequence::find](ds-sequence.find.md) - Пошук індексу за значенням
-   [ДсSequence::first](ds-sequence.first.md) — Повертає перший елемент колекції
-   [ДсSequence::get](ds-sequence.get.md) — Повертає значення за індексом
-   [ДсSequence::insert](ds-sequence.insert.md) — Вставляє значення за вказаним індексом
-   [ДсSequence::join](ds-sequence.join.md) — Склеює всі значення в рядок
-   [ДсSequence::last](ds-sequence.last.md) — Повертає останнє значення колекції
-   [ДсSequence::map](ds-sequence.map.md) — Повертає результат застосування callback-функції до всіх значень колекції
-   [ДсSequence::merge](ds-sequence.merge.md) — Повертає результат додавання всіх заданих значень до колекції
-   [ДсSequence::pop](ds-sequence.pop.md) — Видаляє та повертає останнє значення
-   [ДсSequence::push](ds-sequence.push.md) — Додає значення до кінця послідовності
-   [ДсSequence::reduce](ds-sequence.reduce.md) - Сплескує колекцію до одного значення використовуючи callback-функцію
-   [ДсSequence::remove](ds-sequence.remove.md) — Видаляє та повертає значення за індексом
-   [ДсSequence::reverse](ds-sequence.reverse.md) — Перевертає поточну колекцію
-   [ДсSequence::reversed](ds-sequence.reversed.md) — Повертає перегорнуту копію колекції
-   [ДсSequence::rotate](ds-sequence.rotate.md) — Перемотує послідовність на задану кількість значень
-   [ДсSequence::set](ds-sequence.set.md) — Замінює значення за вказаним індексом
-   [ДсSequence::shift](ds-sequence.shift.md) — Видаляє та повертає перше значення
-   [ДсSequence::slice](ds-sequence.slice.md) — Повертає під-колекцію із заданого діапазону
-   [ДсSequence::sort](ds-sequence.sort.md) — Сортує колекцію
-   [ДсSequence::sorted](ds-sequence.sorted.md) — Повертає копію колекції, відсортовану за значенням.
-   [ДсSequence::sum](ds-sequence.sum.md) — Повертає суму всіх значень колекції
-   [ДсSequence::unshift](ds-sequence.unshift.md) — Додає значення на початок послідовності

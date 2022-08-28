Інтерфейс Sequence

-   [« Ds\\Hashable::hash](ds-hashable.hash.html)
    
-   [Ds\\Sequence::allocate »](ds-sequence.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Інтерфейс Sequence
    

# Інтерфейс Sequence

(No version information available, might only be in Git)

## Вступ

Послідовність описує поведінку, у якому значення розподілені у одному, лінійному порядку. У деяких мовах ця поведінка описується як "List". Це схоже на масив, в якому використовуються цілі ключі, за винятком декількох моментів:

-   Значення завжди проіндексовані по порядку 0, 1, 2, …, size - 1
-   Можна звертатися лише до значень індексованих у діапазоні 0, size - 1

У яких випадках використовується:

-   Якщо ви хочете використовувати масив як список (не звертаючи уваги на ключі).
-   Більш ефективна альтернатива для [SplDoublyLinkedList](class.spldoublylinkedlist.html) і [SplFixedArray](class.splfixedarray.html)

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

| Версия        | Описание                                                  |
|---------------|-----------------------------------------------------------|
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [Ds\\Sequence::allocate](ds-sequence.allocate.html) — Виділення пам'яті під зазначену місткість
-   [Ds\\Sequence::apply](ds-sequence.apply.html) — Оновлення всіх значень застосуванням переданої callback-функції до них
-   [Ds\\Sequence::capacity](ds-sequence.capacity.html) — Повертає поточну місткість
-   [Ds\\Sequence::contains](ds-sequence.contains.html) — Перевіряє, чи містяться в колекції задані значення
-   [Ds\\Sequence::filter](ds-sequence.filter.html) — Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Sequence::find](ds-sequence.find.html) - Пошук індексу за значенням
-   [Ds\\Sequence::first](ds-sequence.first.html) — Повертає перший елемент колекції
-   [Ds\\Sequence::get](ds-sequence.get.html) — Повертає значення за індексом
-   [Ds\\Sequence::insert](ds-sequence.insert.html) — Вставляє значення за вказаним індексом
-   [Ds\\Sequence::join](ds-sequence.join.html) — Склеює всі значення в рядок
-   [Ds\\Sequence::last](ds-sequence.last.html) — Повертає останнє значення колекції
-   [Ds\\Sequence::map](ds-sequence.map.html) — Повертає результат застосування callback-функції до всіх значень колекції
-   [Ds\\Sequence::merge](ds-sequence.merge.html) — Повертає результат додавання всіх заданих значень до колекції
-   [Ds\\Sequence::pop](ds-sequence.pop.html) — Видаляє та повертає останнє значення
-   [Ds\\Sequence::push](ds-sequence.push.html) — Додає значення до кінця послідовності
-   [Ds\\Sequence::reduce](ds-sequence.reduce.html) - Сплескує колекцію до одного значення використовуючи callback-функцію
-   [Ds\\Sequence::remove](ds-sequence.remove.html) — Видаляє та повертає значення за індексом
-   [Ds\\Sequence::reverse](ds-sequence.reverse.html) — Перевертає поточну колекцію
-   [Ds\\Sequence::reversed](ds-sequence.reversed.html) — Повертає перегорнуту копію колекції
-   [Ds\\Sequence::rotate](ds-sequence.rotate.html) — Перемотує послідовність на задану кількість значень
-   [Ds\\Sequence::set](ds-sequence.set.html) — Замінює значення за вказаним індексом
-   [Ds\\Sequence::shift](ds-sequence.shift.html) — Видаляє та повертає перше значення
-   [Ds\\Sequence::slice](ds-sequence.slice.html) — Повертає під-колекцію із заданого діапазону
-   [Ds\\Sequence::sort](ds-sequence.sort.html) — Сортує колекцію
-   [Ds\\Sequence::sorted](ds-sequence.sorted.html) — Повертає копію колекції, відсортовану за значенням.
-   [Ds\\Sequence::sum](ds-sequence.sum.html) — Повертає суму всіх значень колекції
-   [Ds\\Sequence::unshift](ds-sequence.unshift.html) — Додає значення на початок послідовності
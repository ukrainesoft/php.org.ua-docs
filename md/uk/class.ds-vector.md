---
navigation:
  - ds-sequence.unshift.md: '« DsSequence::unshift'
  - ds-vector.allocate.md: 'ДсVector::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Vector
---
# Клас Vector

(No version information available, might only be in Git)

## Вступ

Вектор – це послідовність значень у безперервному буфері, який росте та обрізається автоматично. Це найбільш ефективна послідовна структура, оскільки індекси значень прямо відображаються на їхній індекс у буфері, і фактор зростання не впливає на складність доступу.

## Сильні сторони

-   Підтримує синтаксис масиву (квадратні дужки).
-   Використовує менше пам'яті, ніж масив (array) із тією ж кількістю елементів.
-   Автоматично звільняє пам'ять, коли кількість елементів зменшується.
-   Місткість не обмежена ступенями двійки.
-   **get()** **set()** **push()** і **pop()** мають складність O(1).

## Слабкі сторони

-   **shift()** **unshift()** **insert()** і **remove()** мають складність O(n).

## Огляд класів

```classsynopsis

     
    

    
    

     class Ds\Vector
     implements  Ds\Sequence,  ArrayAccess {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 10;


    /* Методы */
    
   public allocate(int $capacity): void
public apply(callable $callback): void
public capacity(): int
public clear(): void
public contains(mixed ...$values): bool
public copy(): Ds\Vector
public filter(callable $callback = ?): Ds\Vector
public find(mixed $value): mixed
public first(): mixed
public get(int $index): mixed
public insert(int $index, mixed ...$values): void
public isEmpty(): bool
public join(string $glue = ?): string
public last(): mixed
public map(callable $callback): Ds\Vector
public merge(mixed $values): Ds\Vector
public pop(): mixed
public push(mixed ...$values): void
public reduce(callable $callback, mixed $initial = ?): mixed
public remove(int $index): mixed
public reverse(): void
public reversed(): Ds\Vector
public rotate(int $rotations): void
public set(int $index, mixed $value): void
public shift(): mixed
public slice(int $index, int $length = ?): Ds\Vector
public sort(callable $comparator = ?): void
public sorted(callable $comparator = ?): Ds\Vector
public sum(): int|float
public toArray(): array
public unshift(mixed $values = ?): void

   }
```

## Обумовлені константи

**`Ds\Vector::MIN_CAPACITY`**

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсVector::allocate](ds-vector.allocate.md) — Виділяє пам'ять під зазначену місткість
-   [ДсVector::apply](ds-vector.apply.md) - Оновлює всі значення, застосовуючи до них передану callback-функцію
-   [ДсVector::capacity](ds-vector.capacity.md) — Повертає поточну місткість
-   [ДсVector::clear](ds-vector.clear.md) - Видаляє всі значення
-   [ДсVector::construct](ds-vector.construct.md) - Створює новий екземпляр
-   [ДсVector::contains](ds-vector.contains.md) — Перевіряє, чи міститься у векторі задані значення
-   [ДсVector::copy](ds-vector.copy.md) — Повертає поверхневу копію вектора
-   [ДсVector::count](ds-vector.count.md) — Повертає кількість елементів вектора
-   [ДсVector::filter](ds-vector.filter.md) — Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції
-   [ДсVector::find](ds-vector.find.md) - Пошук індексу за значенням
-   [ДсVector::first](ds-vector.first.md) — Повертає перший елемент вектора
-   [ДсVector::get](ds-vector.get.md) — Повертає значення за індексом
-   [ДсVector::insert](ds-vector.insert.md) — Вставляє значення за вказаним індексом
-   [ДсVector::isEmpty](ds-vector.isempty.md) — Перевіряє, чи вектор порожній.
-   [ДсVector::join](ds-vector.join.md) — Склеює всі значення в рядок
-   [ДсVector::jsonSerialize](ds-vector.jsonserialize.md) — Повертає вектор у JSON-представництві
-   [ДсVector::last](ds-vector.last.md) — Повертає останнє значення вектора
-   [ДсVector::map](ds-vector.map.md) — Повертає результат застосування callback-функції до всіх значень вектора
-   [ДсVector::merge](ds-vector.merge.md) — Повертає результат додавання всіх заданих значень у вектор.
-   [ДсVector::pop](ds-vector.pop.md) — Видаляє та повертає останнє значення
-   [ДсVector::push](ds-vector.push.md) — Додає значення до кінця вектора
-   [ДсVector::reduce](ds-vector.reduce.md) - Зменшує вектор до одного значення, використовуючи callback-функцію
-   [ДсVector::remove](ds-vector.remove.md) — Видаляє та повертає значення за індексом
-   [ДсVector::reverse](ds-vector.reverse.md) — Перевертає поточний вектор
-   [ДсVector::reversed](ds-vector.reversed.md) — Повертає перегорнуту копію вектора
-   [ДсVector::rotate](ds-vector.rotate.md) — Перемотує вектор на задану кількість значень
-   [ДсVector::set](ds-vector.set.md) — Замінює значення за вказаним індексом
-   [ДсVector::shift](ds-vector.shift.md) — Видаляє та повертає перше значення
-   [ДсVector::slice](ds-vector.slice.md) — Повертає підвектор із заданого діапазону
-   [ДсVector::sort](ds-vector.sort.md) — Сортує вектор
-   [ДсVector::sorted](ds-vector.sorted.md) — Повертає копію колекції, відсортовану за значенням.
-   [ДсVector::sum](ds-vector.sum.md) — Повертає суму всіх значень колекції
-   [ДсVector::toArray](ds-vector.toarray.md) — Перетворює колекцію на масив (array)
-   [ДсVector::unshift](ds-vector.unshift.md) — Додає значення на початок вектора

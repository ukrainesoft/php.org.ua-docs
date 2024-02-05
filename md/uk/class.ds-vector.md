---
navigation:
  - ds-sequence.unshift.md: '« Ds\\Sequence::unshift'
  - ds-vector.allocate.md: 'Ds\\Vector::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Vector
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Vector

(PECL ds >= 1.0.0)

## Вступ

Вектор – це послідовність значень у безперервному буфері, який росте та обрізається автоматично. Це найбільш ефективна послідовна структура, оскільки індекси значень прямо відображаються на їхній індекс у буфері, і фактор зростання не впливає на складність доступу.

## Сильні сторони

-   Підтримує синтаксис масиву (квадратні дужки).
-   Використовує менше пам'яті, ніж масив (array) із тією ж кількістю елементів.
-   Автоматично звільняє пам'ять, коли кількість елементів зменшується.
-   Місткість не обмежена ступенями двійки.
-   **get()** **set()** \*\*push()** і **pop()\*\*мають складність O(1).

## Слабкі сторони

-   **shift()** **unshift()** \*\*insert()** і **remove()\*\*мають складність O(n).

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

| Версия | Опис |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [Ds\\Vector::allocate](ds-vector.allocate.md)— Виділяє пам'ять під зазначену місткість
-   [Ds\\Vector::apply](ds-vector.apply.md) \- Оновлює всі значення, застосовуючи до них передану callback-функцію
-   [Ds\\Vector::capacity](ds-vector.capacity.md)— Повертає поточну місткість
-   [Ds\\Vector::clear](ds-vector.clear.md) \- Видаляє всі значення
-   [Ds\\Vector::\_\_construct](ds-vector.construct.md) \- Створює новий екземпляр
-   [Ds\\Vector::contains](ds-vector.contains.md)— Перевіряє, чи міститься у векторі задані значення
-   [Ds\\Vector::copy](ds-vector.copy.md)— Повертає поверхневу копію вектора
-   [Ds\\Vector::count](ds-vector.count.md)— Повертає кількість елементів вектора
-   [Ds\\Vector::filter](ds-vector.filter.md)— Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Vector::find](ds-vector.find.md) \- Пошук індексу за значенням
-   [Ds\\Vector::first](ds-vector.first.md)— Повертає перший елемент вектора
-   [Ds\\Vector::get](ds-vector.get.md)— Повертає значення за індексом
-   [Ds\\Vector::insert](ds-vector.insert.md)— Вставляє значення за вказаним індексом
-   [Ds\\Vector::isEmpty](ds-vector.isempty.md)— Перевіряє, чи вектор порожній.
-   [Ds\\Vector::join](ds-vector.join.md) \- Склеює всі значення в рядок
-   [Ds\\Vector::jsonSerialize](ds-vector.jsonserialize.md)— Повертає вектор у JSON-представництві
-   [Ds\\Vector::last](ds-vector.last.md)— Повертає останнє значення вектора
-   [Ds\\Vector::map](ds-vector.map.md)— Повертає результат застосування callback-функції до всіх значень вектора
-   [Ds\\Vector::merge](ds-vector.merge.md)— Повертає результат додавання всіх заданих значень у вектор.
-   [Ds\\Vector::pop](ds-vector.pop.md)— Видаляє та повертає останнє значення
-   [Ds\\Vector::push](ds-vector.push.md)— Додає значення до кінця вектора
-   [Ds\\Vector::reduce](ds-vector.reduce.md) \- Зменшує вектор до одного значення, використовуючи callback-функцію
-   [Ds\\Vector::remove](ds-vector.remove.md)— Видаляє та повертає значення за індексом
-   [Ds\\Vector::reverse](ds-vector.reverse.md)— Перевертає поточний вектор
-   [Ds\\Vector::reversed](ds-vector.reversed.md)— Повертає перегорнуту копію вектора
-   [Ds\\Vector::rotate](ds-vector.rotate.md)— Перемотує вектор на задану кількість значень
-   [Ds\\Vector::set](ds-vector.set.md)— Замінює значення за вказаним індексом
-   [Ds\\Vector::shift](ds-vector.shift.md)— Видаляє та повертає перше значення
-   [Ds\\Vector::slice](ds-vector.slice.md)— Повертає підвектор із заданого діапазону
-   [Ds\\Vector::sort](ds-vector.sort.md)— Сортує вектор
-   [Ds\\Vector::sorted](ds-vector.sorted.md)— Повертає копію колекції, відсортовану за значенням.
-   [Ds\\Vector::sum](ds-vector.sum.md)— Повертає суму всіх значень колекції
-   [Ds\\Vector::toArray](ds-vector.toarray.md)— Перетворює колекцію на масив (array)
-   [Ds\\Vector::unshift](ds-vector.unshift.md)— Додає значення на початок вектора

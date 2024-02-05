---
navigation:
  - ds-vector.unshift.md: '« Ds\\Vector::unshift'
  - ds-deque.allocate.md: 'Ds\\Deque::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Deque
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Deque

(PECL ds >= 1.0.0)

## Вступ

Двостороння черга – це послідовність значень у безперервному буфері, який росте та зменшуються автоматично. Deque (вимовляється як "deck") є абревіатурою від "double-ended queue" і використовується всередині [Ds\\Queue](class.ds-queue.md)

Два покажчики використовуються для відстеження початку та кінця. Покажчики можуть "обернути" кінець черги, що дозволяє уникнути переміщення значень для звільнення місця. Це робить операції shift та unshift такими швидкими, що [Ds\\Vector](class.ds-vector.md) не може з цим змагатися.

Доступ до елемента за індексом вимагає перерахунку залежно від його індексу у буфері: `((head + position) % capacity)`

## Сильні сторони

-   Підтримує синтаксис масиву (квадратні дужки).
-   Потрібно менше пам'яті, ніж масив (array) з тією самою кількістю значень.
-   Автоматично звільняє пам'ять, коли кількість елементів зменшується.
-   **get()** **set()** **push()** **pop()** \*\*shift()**и**unshift()\*\*мають складність O(1).

## Слабкі сторони

-   Місткість обмежена ступенями двійки.
-   \*\*insert()**и**remove()\*\*мають складність O(n).

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Deque
     

     implements 
       Ds\Sequence,  ArrayAccess {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 8;


    /* Методы */
    
   public allocate(int $capacity): void
public apply(callable $callback): void
public capacity(): int
public clear(): void
public contains(mixed ...$values): bool
public copy(): Ds\Deque
public filter(callable $callback = ?): Ds\Deque
public find(mixed $value): mixed
public first(): mixed
public get(int $index): mixed
public insert(int $index, mixed ...$values): void
public isEmpty(): bool
public join(string $glue = ?): string
public last(): mixed
public map(callable $callback): Ds\Deque
public merge(mixed $values): Ds\Deque
public pop(): mixed
public push(mixed ...$values): void
public reduce(callable $callback, mixed $initial = ?): mixed
public remove(int $index): mixed
public reverse(): void
public reversed(): Ds\Deque
public rotate(int $rotations): void
public set(int $index, mixed $value): void
public shift(): mixed
public slice(int $index, int $length = ?): Ds\Deque
public sort(callable $comparator = ?): void
public sorted(callable $comparator = ?): Ds\Deque
public sum(): int|float
public toArray(): array
public unshift(mixed $values = ?): void

   }
```

## Обумовлені константи

**`Ds\Deque::MIN_CAPACITY`**

## список змін

| Версия | Опис |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [Ds\\Deque::allocate](ds-deque.allocate.md)— Виділяє пам'ять під зазначену місткість
-   [Ds\\Deque::apply](ds-deque.apply.md) \- Оновлює всі значення, застосовуючи callback-функцію до кожного значення
-   [Ds\\Deque::capacity](ds-deque.capacity.md)— Повертає поточну місткість
-   [Ds\\Deque::clear](ds-deque.clear.md)— Видаляє всі значення із двосторонньої черги
-   [Ds\\Deque::\_\_construct](ds-deque.construct.md) \- Створює новий екземпляр
-   [Ds\\Deque::contains](ds-deque.contains.md)— Перевіряє, чи є у двосторонній черзі задані значення
-   [Ds\\Deque::copy](ds-deque.copy.md)— Повертає поверхневу копію колекції
-   [Ds\\Deque::count](ds-deque.count.md)— Повертає кількість елементів двосторонньої черги
-   [Ds\\Deque::filter](ds-deque.filter.md)— Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Deque::find](ds-deque.find.md) \- Пошук індексу за значенням
-   [Ds\\Deque::first](ds-deque.first.md)— Повертає перший елемент двосторонньої черги
-   [Ds\\Deque::get](ds-deque.get.md)— Повертає значення за індексом
-   [Ds\\Deque::insert](ds-deque.insert.md)— Вставляє значення за вказаним індексом
-   [Ds\\Deque::isEmpty](ds-deque.isempty.md)— Перевіряє, чи порожня двостороння черга
-   [Ds\\Deque::join](ds-deque.join.md) \- Склеює всі значення в рядок
-   [Ds\\Deque::jsonSerialize](ds-deque.jsonserialize.md)— Повертає колекцію в JSON-представництві
-   [Ds\\Deque::last](ds-deque.last.md)— Повертає останнє значення двосторонньої черги
-   [Ds\\Deque::map](ds-deque.map.md)— Повертає результат застосування callback-функції до всіх значень двосторонньої черги
-   [Ds\\Deque::merge](ds-deque.merge.md)— Повертає результат додавання всіх заданих значень у двосторонню чергу
-   [Ds\\Deque::pop](ds-deque.pop.md)— Видаляє та повертає останнє значення
-   [Ds\\Deque::push](ds-deque.push.md)— Додає значення наприкінці двосторонньої черги
-   [Ds\\Deque::reduce](ds-deque.reduce.md) \- Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [Ds\\Deque::remove](ds-deque.remove.md)— Видаляє та повертає значення за індексом
-   [Ds\\Deque::reverse](ds-deque.reverse.md)— Перевертає поточну двосторонню чергу
-   [Ds\\Deque::reversed](ds-deque.reversed.md)— Повертає перегорнуту копію двосторонньої черги
-   [Ds\\Deque::rotate](ds-deque.rotate.md)— Перемотує двосторонню чергу на задану кількість значень
-   [Ds\\Deque::set](ds-deque.set.md)— Замінює значення за вказаним індексом
-   [Ds\\Deque::shift](ds-deque.shift.md)— Видаляє та повертає перше значення
-   [Ds\\Deque::slice](ds-deque.slice.md)— Повертає почергово із заданого діапазону
-   [Ds\\Deque::sort](ds-deque.sort.md)— Сортує двосторонню чергу
-   [Ds\\Deque::sorted](ds-deque.sorted.md)— Повертає відсортовану за значенням копію двосторонньої черги
-   [Ds\\Deque::sum](ds-deque.sum.md)— Повертає суму всіх значень двосторонньої черги
-   [Ds\\Deque::toArray](ds-deque.toarray.md) \- Перетворює двосторонню чергу на масив (array)
-   [Ds\\Deque::unshift](ds-deque.unshift.md)— Додає значення на початок двосторонньої черги

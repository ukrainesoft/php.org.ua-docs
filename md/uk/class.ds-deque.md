---
navigation:
  - ds-vector.unshift.html: '« DsVector::unshift'
  - ds-deque.allocate.html: 'ДсDeque::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Deque
---
# Клас Deque

(No version information available, might only be in Git)

## Вступ

Двостороння черга – це послідовність значень у безперервному буфері, який росте та зменшуються автоматично. Deque (вимовляється як "deck") є абревіатурою від "double-ended queue" і використовується всередині **ДсQueue**

Два покажчики використовуються для відстеження початку та кінця. Покажчики можуть "обернути" кінець черги, що дозволяє уникнути переміщення значень для звільнення місця. Це робить операції shift та unshift такими швидкими, що **ДсVector** не може з цим змагатися.

Доступ до елемента за індексом вимагає перерахунку залежно від його індексу у буфері: `((head + position) % capacity)`

## Сильні сторони

-   Підтримує синтаксис масиву (квадратні дужки).
-   Вимагає менше пам'яті, ніж масив (array) з тією самою кількістю значень.
-   Автоматично звільняє пам'ять, коли кількість елементів зменшується.
-   **get()** **set()** **push()** **pop()** **shift()** і **unshift()** мають складність O(1).

## Слабкі сторони

-   Місткість обмежена ступенями двійки.
-   **insert()** і **remove()** мають складність O(n).

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

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсDeque::allocate](ds-deque.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [ДсDeque::apply](ds-deque.apply.html) - Оновлює всі значення, застосовуючи callback-функцію до кожного значення
-   [ДсDeque::capacity](ds-deque.capacity.html) — Повертає поточну місткість
-   [ДсDeque::clear](ds-deque.clear.html) — Видаляє всі значення із двосторонньої черги
-   [ДсDeque::construct](ds-deque.construct.html) - Створює новий екземпляр
-   [ДсDeque::contains](ds-deque.contains.html) — Перевіряє, чи є у двосторонній черзі задані значення
-   [ДсDeque::copy](ds-deque.copy.html) — Повертає поверхневу копію колекції
-   [ДсDeque::count](ds-deque.count.html) — Повертає кількість елементів двосторонньої черги
-   [ДсDeque::filter](ds-deque.filter.html) — Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції
-   [ДсDeque::find](ds-deque.find.html) - Пошук індексу за значенням
-   [ДсDeque::first](ds-deque.first.html) — Повертає перший елемент двосторонньої черги
-   [ДсDeque::get](ds-deque.get.html) — Повертає значення за індексом
-   [ДсDeque::insert](ds-deque.insert.html) — Вставляє значення за вказаним індексом
-   [ДсDeque::isEmpty](ds-deque.isempty.html) — Перевіряє, чи порожня двостороння черга
-   [ДсDeque::join](ds-deque.join.html) - Склеює всі значення в рядок
-   [ДсDeque::jsonSerialize](ds-deque.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [ДсDeque::last](ds-deque.last.html) — Повертає останнє значення двосторонньої черги
-   [ДсDeque::map](ds-deque.map.html) — Повертає результат застосування callback-функції до всіх значень двосторонньої черги
-   [ДсDeque::merge](ds-deque.merge.html) — Повертає результат додавання всіх заданих значень у двосторонню чергу
-   [ДсDeque::pop](ds-deque.pop.html) — Видаляє та повертає останнє значення
-   [ДсDeque::push](ds-deque.push.html) — Додає значення наприкінці двосторонньої черги
-   [ДсDeque::reduce](ds-deque.reduce.html) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [ДсDeque::remove](ds-deque.remove.html) — Видаляє та повертає значення за індексом
-   [ДсDeque::reverse](ds-deque.reverse.html) — Перевертає поточну двосторонню чергу
-   [ДсDeque::reversed](ds-deque.reversed.html) — Повертає перегорнуту копію двосторонньої черги
-   [ДсDeque::rotate](ds-deque.rotate.html) — Перемотує двосторонню чергу на задану кількість значень
-   [ДсDeque::set](ds-deque.set.html) — Замінює значення за вказаним індексом
-   [ДсDeque::shift](ds-deque.shift.html) — Видаляє та повертає перше значення
-   [ДсDeque::slice](ds-deque.slice.html) — Повертає почергово із заданого діапазону
-   [ДсDeque::sort](ds-deque.sort.html) — Сортує двосторонню чергу
-   [ДсDeque::sorted](ds-deque.sorted.html) — Повертає відсортовану за значенням копію двосторонньої черги
-   [ДсDeque::sum](ds-deque.sum.html) — Повертає суму всіх значень двосторонньої черги
-   [ДсDeque::toArray](ds-deque.toarray.html) - Перетворює двосторонню чергу на масив (array)
-   [ДсDeque::unshift](ds-deque.unshift.html) — Додає значення на початок двосторонньої черги

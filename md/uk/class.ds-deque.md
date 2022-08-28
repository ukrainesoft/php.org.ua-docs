Клас Deque

-   [« Ds\\Vector::unshift](ds-vector.unshift.html)
    
-   [Ds\\Deque::allocate »](ds-deque.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас Deque
    

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

| Версия        | Описание                                                  |
|---------------|-----------------------------------------------------------|
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [Ds\\Deque::allocate](ds-deque.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [Ds\\Deque::apply](ds-deque.apply.html) - Оновлює всі значення, застосовуючи callback-функцію до кожного значення
-   [Ds\\Deque::capacity](ds-deque.capacity.html) — Повертає поточну місткість
-   [Ds\\Deque::clear](ds-deque.clear.html) — Видаляє всі значення із двосторонньої черги
-   [Ds\\Deque::\_\_construct](ds-deque.construct.html) - Створює новий екземпляр
-   [Ds\\Deque::contains](ds-deque.contains.html) — Перевіряє, чи є у двосторонній черзі задані значення
-   [Ds\\Deque::copy](ds-deque.copy.html) — Повертає поверхневу копію колекції
-   [Ds\\Deque::count](ds-deque.count.html) — Повертає кількість елементів двосторонньої черги
-   [Ds\\Deque::filter](ds-deque.filter.html) — Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Deque::find](ds-deque.find.html) - Пошук індексу за значенням
-   [Ds\\Deque::first](ds-deque.first.html) — Повертає перший елемент двосторонньої черги
-   [Ds\\Deque::get](ds-deque.get.html) — Повертає значення за індексом
-   [Ds\\Deque::insert](ds-deque.insert.html) — Вставляє значення за вказаним індексом
-   [Ds\\Deque::isEmpty](ds-deque.isempty.html) — Перевіряє, чи порожня двостороння черга
-   [Ds\\Deque::join](ds-deque.join.html) - Склеює всі значення в рядок
-   [Ds\\Deque::jsonSerialize](ds-deque.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [Ds\\Deque::last](ds-deque.last.html) — Повертає останнє значення двосторонньої черги
-   [Ds\\Deque::map](ds-deque.map.html) — Повертає результат застосування callback-функції до всіх значень двосторонньої черги
-   [Ds\\Deque::merge](ds-deque.merge.html) — Повертає результат додавання всіх заданих значень у двосторонню чергу
-   [Ds\\Deque::pop](ds-deque.pop.html) — Видаляє та повертає останнє значення
-   [Ds\\Deque::push](ds-deque.push.html) — Додає значення наприкінці двосторонньої черги
-   [Ds\\Deque::reduce](ds-deque.reduce.html) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [Ds\\Deque::remove](ds-deque.remove.html) — Видаляє та повертає значення за індексом
-   [Ds\\Deque::reverse](ds-deque.reverse.html) — Перевертає поточну двосторонню чергу
-   [Ds\\Deque::reversed](ds-deque.reversed.html) — Повертає перегорнуту копію двосторонньої черги
-   [Ds\\Deque::rotate](ds-deque.rotate.html) — Перемотує двосторонню чергу на задану кількість значень
-   [Ds\\Deque::set](ds-deque.set.html) — Замінює значення за вказаним індексом
-   [Ds\\Deque::shift](ds-deque.shift.html) — Видаляє та повертає перше значення
-   [Ds\\Deque::slice](ds-deque.slice.html) — Повертає почергово із заданого діапазону
-   [Ds\\Deque::sort](ds-deque.sort.html) — Сортує двосторонню чергу
-   [Ds\\Deque::sorted](ds-deque.sorted.html) — Повертає відсортовану за значенням копію двосторонньої черги
-   [Ds\\Deque::sum](ds-deque.sum.html) — Повертає суму всіх значень двосторонньої черги
-   [Ds\\Deque::toArray](ds-deque.toarray.html) - Перетворює двосторонню чергу на масив (array)
-   [Ds\\Deque::unshift](ds-deque.unshift.html) — Додає значення на початок двосторонньої черги
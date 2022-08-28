Клас Map

-   [« Ds\\Deque::unshift](ds-deque.unshift.html)
    
-   [Ds\\Map::allocate »](ds-map.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас Map
    

# Клас Map

(No version information available, might only be in Git)

## Вступ

Колекція пар - це послідовна колекція, що містить пари ключ-значення, практично ідентична масиву і використовується для тих же цілей. Ключі можуть бути будь-якого типу, але мають бути унікальними. Якщо додати пару з існуючим ключем, то вона буде замінена.

## Сильні сторони

-   Ключі та значення можуть бути будь-якого типу, включаючи об'єкти.
-   Підтримує синтаксис масиву (квадратні дужки).
-   Зберігається порядок вставки.
-   Швидкість та споживання пам'яті можна порівняти з використанням масиву.
-   Автоматично звільняє пам'ять, коли кількість елементів зменшується.

## Слабкі сторони

-   Не може бути конвертована в масив, якщо як ключі використовуються об'єкти.

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Map
     

     implements 
       Ds\Collection,  ArrayAccess {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 16;


    /* Методы */
    
   public allocate(int $capacity): void
public apply(callable $callback): void
public capacity(): int
public clear(): void
public copy(): Ds\Map
public diff(Ds\Map $map): Ds\Map
public filter(callable $callback = ?): Ds\Map
public first(): Ds\Pair
public get(mixed $key, mixed $default = ?): mixed
public hasKey(mixed $key): bool
public hasValue(mixed $value): bool
public intersect(Ds\Map $map): Ds\Map
public isEmpty(): bool
public keys(): Ds\Set
public ksort(callable $comparator = ?): void
public ksorted(callable $comparator = ?): Ds\Map
public last(): Ds\Pair
public map(callable $callback): Ds\Map
public merge(mixed $values): Ds\Map
public pairs(): Ds\Sequence
public put(mixed $key, mixed $value): void
public putAll(mixed $pairs): void
public reduce(callable $callback, mixed $initial = ?): mixed
public remove(mixed $key, mixed $default = ?): mixed
public reverse(): void
public reversed(): Ds\Map
public skip(int $position): Ds\Pair
public slice(int $index, int $length = ?): Ds\Map
public sort(callable $comparator = ?): void
public sorted(callable $comparator = ?): Ds\Map
public sum(): int|float
public toArray(): array
public union(Ds\Map $map): Ds\Map
public values(): Ds\Sequence
public xor(Ds\Map $map): Ds\Map

   }
```

## Обумовлені константи

**`Ds\Map::MIN_CAPACITY`**

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [Ds\\Map::allocate](ds-map.allocate.html) — Виділяє необхідну кількість пам'яті під потрібну місткість
-   [Ds\\Map::apply](ds-map.apply.html) — Оновлення всіх значень застосуванням переданої callback-функції до них
-   [Ds\\Map::capacity](ds-map.capacity.html) — Повертає поточну місткість
-   [Ds\\Map::clear](ds-map.clear.html) — Видаляє всі значення з колекції
-   [Ds\\Map::\_\_construct](ds-map.construct.html) - Створює новий екземпляр
-   [Ds\\Map::copy](ds-map.copy.html) — Повертає поверхневу копію колекції
-   [Ds\\Map::count](ds-map.count.html) — Повертає кількість елементів колекції
-   [Ds\\Map::diff](ds-map.diff.html) — Створює нову колекцію пар із елементами, ключів яких немає в іншій колекції пар
-   [Ds\\Map::filter](ds-map.filter.html) — Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції
-   [Ds\\Map::first](ds-map.first.html) — Повертає перший елемент колекції
-   [Ds\\Map::get](ds-map.get.html) — Повертає значення за ключом
-   [Ds\\Map::hasKey](ds-map.haskey.html) — Перевіряє, чи колекція містить заданий ключ
-   [Ds\\Map::hasValue](ds-map.hasvalue.html) — Перевіряє, чи колекція містить задане значення
-   [Ds\\Map::intersect](ds-map.intersect.html) — Створює нову колекцію пар, створену перетином з іншою колекцією пар
-   [Ds\\Map::isEmpty](ds-map.isempty.html) — Перевіряє, чи колекція порожня.
-   [Ds\\Map::jsonSerialize](ds-map.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [Ds\\Map::keys](ds-map.keys.html) — Повертає набір ключів колекції
-   [Ds\\Map::ksort](ds-map.ksort.html) — Сортує поточну колекцію за ключами
-   [Ds\\Map::ksorted](ds-map.ksorted.html) — Повертає копію колекції, відсортованої за ключами
-   [Ds\\Map::last](ds-map.last.html) — Повертає останню пару колекції
-   [Ds\\Map::map](ds-map.map.html) — Повертає результат застосування callback-функції до всіх значень колекції.
-   [Ds\\Map::merge](ds-map.merge.html) — Повертає результат додавання всіх заданих елементів до колекції
-   [Ds\\Map::pairs](ds-map.pairs.html) — Повертає послідовність, яка містить усі пари колекції.
-   [Ds\\Map::put](ds-map.put.html) — Встановлення значення за заданим ключем
-   [Ds\\Map::putAll](ds-map.putall.html) — Зв'язує з колекцією всі пари ключ-значення з об'єкту класу traversable чи масиву
-   [Ds\\Map::reduce](ds-map.reduce.html) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [Ds\\Map::remove](ds-map.remove.html) — Видаляє та повертає значення за ключом
-   [Ds\\Map::reverse](ds-map.reverse.html) — Перевертає поточну колекцію
-   [Ds\\Map::reversed](ds-map.reversed.html) — Повертає перегорнуту копію колекції
-   [Ds\\Map::skip](ds-map.skip.html) — Повертає пару за індексом позиції
-   [Ds\\Map::slice](ds-map.slice.html) — Повертає підмножину колекції із заданого діапазону
-   [Ds\\Map::sort](ds-map.sort.html) — Сортує колекцію за значеннями
-   [Ds\\Map::sorted](ds-map.sorted.html) — Повертає копію колекції, відсортовану за значенням.
-   [Ds\\Map::sum](ds-map.sum.html) — Повертає суму всіх значень колекції
-   [Ds\\Map::toArray](ds-map.toarray.html) — Перетворює колекцію на array
-   [Ds\\Map::union](ds-map.union.html) — Створює нову колекцію пар із елементів двох колекцій
-   [Ds\\Map::values](ds-map.values.html) — Повертає послідовність значень колекції
-   [Ds\\Map::xor](ds-map.xor.html) — Створює нову колекцію пар із елементів, які є в одній із колекцій, але не в обох одночасно
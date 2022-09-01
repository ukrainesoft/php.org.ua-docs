---
navigation:
  - ds-deque.unshift.html: '« DsDeque::unshift'
  - ds-map.allocate.html: 'ДсMap::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Map
---
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
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсMap::allocate](ds-map.allocate.md) — Виділяє необхідну кількість пам'яті під потрібну місткість
-   [ДсMap::apply](ds-map.apply.md) — Оновлення всіх значень застосуванням переданої callback-функції до них
-   [ДсMap::capacity](ds-map.capacity.md) — Повертає поточну місткість
-   [ДсMap::clear](ds-map.clear.md) — Видаляє всі значення з колекції
-   [ДсMap::construct](ds-map.construct.md) - Створює новий екземпляр
-   [ДсMap::copy](ds-map.copy.md) — Повертає поверхневу копію колекції
-   [ДсMap::count](ds-map.count.md) — Повертає кількість елементів колекції
-   [ДсMap::diff](ds-map.diff.md) — Створює нову колекцію пар із елементами, ключів яких немає в іншій колекції пар
-   [ДсMap::filter](ds-map.filter.md) — Створює нову колекцію пар із елементів, вибраних за допомогою заданої callback-функції
-   [ДсMap::first](ds-map.first.md) — Повертає перший елемент колекції
-   [ДсMap::get](ds-map.get.md) — Повертає значення за ключом
-   [ДсMap::hasKey](ds-map.haskey.md) — Перевіряє, чи колекція містить заданий ключ
-   [ДсMap::hasValue](ds-map.hasvalue.md) — Перевіряє, чи колекція містить задане значення
-   [ДсMap::intersect](ds-map.intersect.md) — Створює нову колекцію пар, створену перетином з іншою колекцією пар
-   [ДсMap::isEmpty](ds-map.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсMap::jsonSerialize](ds-map.jsonserialize.md) — Повертає колекцію в JSON-представництві
-   [ДсMap::keys](ds-map.keys.md) — Повертає набір ключів колекції
-   [ДсMap::ksort](ds-map.ksort.md) — Сортує поточну колекцію за ключами
-   [ДсMap::ksorted](ds-map.ksorted.md) — Повертає копію колекції, відсортованої за ключами
-   [ДсMap::last](ds-map.last.md) — Повертає останню пару колекції
-   [ДсMap::map](ds-map.map.md) — Повертає результат застосування callback-функції до всіх значень колекції.
-   [ДсMap::merge](ds-map.merge.md) — Повертає результат додавання всіх заданих елементів до колекції
-   [ДсMap::pairs](ds-map.pairs.md) — Повертає послідовність, яка містить усі пари колекції.
-   [ДсMap::put](ds-map.put.md) — Встановлення значення за заданим ключем
-   [ДсMap::putAll](ds-map.putall.md) — Зв'язує з колекцією всі пари ключ-значення з об'єкту класу traversable чи масиву
-   [ДсMap::reduce](ds-map.reduce.md) - Зменшує колекцію до одного значення, використовуючи callback-функцію
-   [ДсMap::remove](ds-map.remove.md) — Видаляє та повертає значення за ключом
-   [ДсMap::reverse](ds-map.reverse.md) — Перевертає поточну колекцію
-   [ДсMap::reversed](ds-map.reversed.md) — Повертає перегорнуту копію колекції
-   [ДсMap::skip](ds-map.skip.md) — Повертає пару за індексом позиції
-   [ДсMap::slice](ds-map.slice.md) — Повертає підмножину колекції із заданого діапазону
-   [ДсMap::sort](ds-map.sort.md) — Сортує колекцію за значеннями
-   [ДсMap::sorted](ds-map.sorted.md) — Повертає копію колекції, відсортовану за значенням.
-   [ДсMap::sum](ds-map.sum.md) — Повертає суму всіх значень колекції
-   [ДсMap::toArray](ds-map.toarray.md) — Перетворює колекцію на array
-   [ДсMap::union](ds-map.union.md) — Створює нову колекцію пар із елементів двох колекцій
-   [ДсMap::values](ds-map.values.md) — Повертає послідовність значень колекції
-   [ДсMap::xor](ds-map.xor.md) — Створює нову колекцію пар із елементів, які є в одній із колекцій, але не в обох одночасно

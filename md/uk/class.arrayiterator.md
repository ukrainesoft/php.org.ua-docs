---
navigation:
  - appenditerator.valid.md: '« AppendIterator::valid'
  - arrayiterator.append.md: 'ArrayIterator::append »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас ArrayIterator
---
# Клас ArrayIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей ітератор дозволяє скидати та модифікувати значення та ключі в процесі ітерації за масивами та об'єктами.

Коли ви хочете перебрати один і той же масив кілька разів, вам потрібно створити екземпляр ArrayObject і створити для нього об'єкти ArrayIterator, які посилаються на нього або за допомогою [foreach](control-structures.foreach.md) або під час виклику методу getIterator() вручну.

## Огляд класів

```classsynopsis

     
    

    
     
      class ArrayIterator
     

     implements 
       SeekableIterator,  ArrayAccess,  Serializable,  Countable {

    /* Константы */
    
     const
     int
      STD_PROP_LIST = 1;

    const
     int
      ARRAY_AS_PROPS = 2;


    /* Методы */
    
   public __construct(array|object $array = [], int $flags = 0)

    public append(mixed $value): void
public asort(int $flags = SORT_REGULAR): bool
public count(): int
public current(): mixed
public getArrayCopy(): array
public getFlags(): int
public key(): string|int|null
public ksort(int $flags = SORT_REGULAR): bool
public natcasesort(): bool
public natsort(): bool
public next(): void
public offsetExists(mixed $key): bool
public offsetGet(mixed $key): mixed
public offsetSet(mixed $key, mixed $value): void
public offsetUnset(mixed $key): void
public rewind(): void
public seek(int $offset): void
public serialize(): string
public setFlags(int $flags): void
public uasort(callable $callback): bool
public uksort(callable $callback): bool
public unserialize(string $data): void
public valid(): bool

   }
```

## Обумовлені константи

## Прапори ArrayIterator

**`ArrayIterator::STD_PROP_LIST`**

Властивості мають звичайну функціональність при доступі у вигляді списку (vardump, foreach і т.д.).

**`ArrayIterator::ARRAY_AS_PROPS`**

Записи можуть бути доступні як властивості (читання та запис).

## Зміст

-   [ArrayIterator::append](arrayiterator.append.md) - Додати елемент
-   [ArrayIterator::asort](arrayiterator.asort.md) — Сортує елементи за значеннями
-   [ArrayIterator::construct](arrayiterator.construct.md) - Створює ArrayIterator
-   [ArrayIterator::count](arrayiterator.count.md) — Порахувати кількість елементів
-   [ArrayIterator::current](arrayiterator.current.md) — Повертає поточний елемент у масиві
-   [ArrayIterator::getArrayCopy](arrayiterator.getarraycopy.md) — Повертає копію масиву
-   [ArrayIterator::getFlags](arrayiterator.getflags.md) — Отримує прапори поведінки
-   [ArrayIterator::key](arrayiterator.key.md) — Повертає ключ поточного елемента масиву
-   [ArrayIterator::ksort](arrayiterator.ksort.md) — Сортує елементи за ключами
-   [ArrayIterator::natcasesort](arrayiterator.natcasesort.md) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort](arrayiterator.natsort.md) - Сортує елементи "натурально"
-   [ArrayIterator::next](arrayiterator.next.md) — Переміщує покажчик за наступний запис
-   [ArrayIterator::offsetExists](arrayiterator.offsetexists.md) — Перевіряє, чи існує зміщення
-   [ArrayIterator::offsetGet](arrayiterator.offsetget.md) — Отримує значення для усунення
-   [ArrayIterator::offsetSet](arrayiterator.offsetset.md) — Встановлює значення для усунення
-   [ArrayIterator::offsetUnset](arrayiterator.offsetunset.md) — Скидає значення зі зміщення
-   [ArrayIterator::rewind](arrayiterator.rewind.md) — Переміщує покажчик на початок масиву
-   [ArrayIterator::seek](arrayiterator.seek.md) — Переміщує курсор на вибрану позицію
-   [ArrayIterator::serialize](arrayiterator.serialize.md) - Серіалізує масив
-   [ArrayIterator::setFlags](arrayiterator.setflags.md) - Встановлює прапори, що змінюють поведінку ArrayIterator
-   [ArrayIterator::uasort](arrayiterator.uasort.md) — Сортування за допомогою заданої користувачем функції та збереження ключів
-   [ArrayIterator::uksort](arrayiterator.uksort.md) — Сортування за ключами за допомогою заданої функції порівняння
-   [ArrayIterator::unserialize](arrayiterator.unserialize.md) - Десеріалізація
-   [ArrayIterator::valid](arrayiterator.valid.md) — Перевіряє, чи масив містить ще записи

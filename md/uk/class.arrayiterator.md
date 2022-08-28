Клас ArrayIterator

-   [« AppendIterator::valid](appenditerator.valid.html)
    
-   [ArrayIterator::append »](arrayiterator.append.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас ArrayIterator
    

# Клас ArrayIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей ітератор дозволяє скидати та модифікувати значення та ключі в процесі ітерації за масивами та об'єктами.

Коли ви хочете перебрати один і той же масив кілька разів, вам потрібно створити екземпляр ArrayObject і створити для нього об'єкти ArrayIterator, які посилаються на нього або за допомогою [foreach](control-structures.foreach.html) або під час виклику методу getIterator() вручну.

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

-   [ArrayIterator::append](arrayiterator.append.html) - Додати елемент
-   [ArrayIterator::asort](arrayiterator.asort.html) — Сортує елементи за значеннями
-   [ArrayIterator::\_\_construct](arrayiterator.construct.html) - Створює ArrayIterator
-   [ArrayIterator::count](arrayiterator.count.html) — Порахувати кількість елементів
-   [ArrayIterator::current](arrayiterator.current.html) — Повертає поточний елемент у масиві
-   [ArrayIterator::getArrayCopy](arrayiterator.getarraycopy.html) — Повертає копію масиву
-   [ArrayIterator::getFlags](arrayiterator.getflags.html) — Отримує прапори поведінки
-   [ArrayIterator::key](arrayiterator.key.html) — Повертає ключ поточного елемента масиву
-   [ArrayIterator::ksort](arrayiterator.ksort.html) — Сортує елементи за ключами
-   [ArrayIterator::natcasesort](arrayiterator.natcasesort.html) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort](arrayiterator.natsort.html) - Сортує елементи "натурально"
-   [ArrayIterator::next](arrayiterator.next.html) — Переміщує покажчик за наступний запис
-   [ArrayIterator::offsetExists](arrayiterator.offsetexists.html) — Перевіряє, чи існує зміщення
-   [ArrayIterator::offsetGet](arrayiterator.offsetget.html) — Отримує значення для усунення
-   [ArrayIterator::offsetSet](arrayiterator.offsetset.html) — Встановлює значення для усунення
-   [ArrayIterator::offsetUnset](arrayiterator.offsetunset.html) — Скидає значення зі зміщення
-   [ArrayIterator::rewind](arrayiterator.rewind.html) — Переміщує покажчик на початок масиву
-   [ArrayIterator::seek](arrayiterator.seek.html) — Переміщує курсор на вибрану позицію
-   [ArrayIterator::serialize](arrayiterator.serialize.html) - Серіалізує масив
-   [ArrayIterator::setFlags](arrayiterator.setflags.html) - Встановлює прапори, що змінюють поведінку ArrayIterator
-   [ArrayIterator::uasort](arrayiterator.uasort.html) — Сортування за допомогою заданої користувачем функції та збереження ключів
-   [ArrayIterator::uksort](arrayiterator.uksort.html) — Сортування за ключами за допомогою заданої функції порівняння
-   [ArrayIterator::unserialize](arrayiterator.unserialize.html) - Десеріалізація
-   [ArrayIterator::valid](arrayiterator.valid.html) — Перевіряє, чи масив містить ще записи
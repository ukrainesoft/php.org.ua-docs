Клас MultipleIterator

-   [« LimitIterator::valid](limititerator.valid.html)
    
-   [MultipleIterator::attachIterator »](multipleiterator.attachiterator.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас MultipleIterator
    

# Клас MultipleIterator

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Ітератор, який послідовно перебирає за всіма приєднаними ітераторами

## Огляд класів

```classsynopsis

     
    

    
     
      class MultipleIterator
     

     implements 
       Iterator {

    /* Константы */
    
     const
     int
      MIT_NEED_ANY = 0;

    const
     int
      MIT_NEED_ALL = 1;

    const
     int
      MIT_KEYS_NUMERIC = 0;

    const
     int
      MIT_KEYS_ASSOC = 2;


    /* Методы */
    
   public __construct(int $flags = MultipleIterator::MIT_NEED_ALL | MultipleIterator::MIT_KEYS_NUMERIC)

    public attachIterator(Iterator $iterator, string|int|null $info = null): void
public containsIterator(Iterator $iterator): bool
public countIterators(): int
public current(): array
public detachIterator(Iterator $iterator): void
public getFlags(): int
public key(): array
public next(): void
public rewind(): void
public setFlags(int $flags): void
public valid(): bool

   }
```

## Обумовлені константи

**`MultipleIterator::MIT_NEED_ANY`**

Не вимагати, щоб усі підитератори були дійсними в ітерації.

**`MultipleIterator::MIT_NEED_ALL`**

Вимагати, щоб усі підитератори були дійсними в ітерації.

**`MultipleIterator::MIT_KEYS_NUMERIC`**

Ключі створюються з позиції підитераторів.

**`MultipleIterator::MIT_KEYS_ASSOC`**

Ключі створюються із пов'язаної з подитераторами інформації.

## Зміст

-   [MultipleIterator::attachIterator](multipleiterator.attachiterator.html) - Приєднує ітератор
-   [MultipleIterator::\_\_construct](multipleiterator.construct.html) — Створює новий MultipleIterator
-   [MultipleIterator::containsIterator](multipleiterator.containsiterator.html) — Перевіряє, чи приєднано ітератора.
-   [MultipleIterator::countIterators](multipleiterator.countiterators.html) — Отримує кількість приєднаних ітераторів
-   [MultipleIterator::current](multipleiterator.current.html) — Отримує зареєстровані ітератори
-   [MultipleIterator::detachIterator](multipleiterator.detachiterator.html) - Від'єднує ітератор
-   [MultipleIterator::getFlags](multipleiterator.getflags.html) — Отримує інформацію про прапори
-   [MultipleIterator::key](multipleiterator.key.html) — Отримує зареєстровані ітератори
-   [MultipleIterator::next](multipleiterator.next.html) — Переміщує всі приєднані ітератори до наступних елементів.
-   [MultipleIterator::rewind](multipleiterator.rewind.html) — Повертає на початок усі приєднані ітератори
-   [MultipleIterator::setFlags](multipleiterator.setflags.html) - Встановлює прапори
-   [MultipleIterator::valid](multipleiterator.valid.html) - Перевіряє коректність підитераторів
Клас APCUIterator

-   [« apcu\_store](function.apcu-store.html)
    
-   [APCUIterator::\_\_construct »](apcuiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [APCu](book.apcu.html)
    
-   Клас APCUIterator
    

# Клас APCUIterator

(PECL apcu >= 5.0.0)

## Вступ

Клас **APCUIterator** дозволяє легко ітерувати великий APCu кеш. Це корисно, оскільки дозволяє перебирати великий кеш по кроках, забираючи задану кількість записів, використовуючи одне блокування, дозволяючи іншим активностям використовувати блокування, а не затримувати весь кеш для читання ста (за замовчуванням) записів. Також, використання регулярних виразів ефективніше, оскільки виконується лише на рівні скомпилированного коду C.

## Огляд класів

```classsynopsis


    
    
     
      class APCUIterator
     

     implements 
       Iterator {
    

    /* Методы */
    
   public __construct(    array|string|null $search = null,    int $format = APC_ITER_ALL,    int $chunk_size = 100,    int $list = APC_LIST_ACTIVE)

    public current(): mixed
public getTotalCount(): int
public getTotalHits(): int
public getTotalSize(): int
public key(): string
public next(): bool
public rewind(): void
public valid(): bool

   }
```

## Зміст

-   [APCUIterator::\_\_construct](apcuiterator.construct.html) — Створює об'єкт ітератора класу APCUIterator
-   [APCUIterator::current](apcuiterator.current.html) — Отримати поточний елемент
-   [APCUIterator::getTotalCount](apcuiterator.gettotalcount.html) — Отримати загальну кількість записів
-   [APCUIterator::getTotalHits](apcuiterator.gettotalhits.html) — Отримати загальну кількість попадань у кеш
-   [APCUIterator::getTotalSize](apcuiterator.gettotalsize.html) - Загальний розмір кешу
-   [APCUIterator::key](apcuiterator.key.html) - Отримати ключ ітератора
-   [APCUIterator::next](apcuiterator.next.html) — Переміщує курсор на наступний елемент
-   [APCUIterator::rewind](apcuiterator.rewind.html) - Перемотування ітератора
-   [APCUIterator::valid](apcuiterator.valid.html) — Перевіряє, чи поточна позиція ітератора коректна.
---
navigation:
  - function.apcu-store.md: « apcu\_store
  - apcuiterator.construct.md: 'APCUIterator::\_\_construct »'
  - index.md: PHP Manual
  - book.apcu.md: APCu
title: Клас APCUIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас APCUIterator

(PECL apcu >= 5.0.0)

## Вступ

Класс**APCUIterator** дозволяє легко ітерувати великий APCu кеш. Це корисно, оскільки дозволяє перебирати великий кеш по кроках, забираючи задану кількість записів, використовуючи одне блокування, дозволяючи іншим активностям використовувати блокування, а не затримувати весь кеш для читання ста (за замовчуванням) записів. Також, використання регулярних виразів ефективніше, оскільки виконується лише на рівні скомпилированного коду C.

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

-   [APCUIterator::\_\_construct](apcuiterator.construct.md)— Створює об'єкт ітератора класу APCUIterator
-   [APCUIterator::current](apcuiterator.current.md)— Отримати поточний елемент
-   [APCUIterator::getTotalCount](apcuiterator.gettotalcount.md)— Отримати загальну кількість записів
-   [APCUIterator::getTotalHits](apcuiterator.gettotalhits.md)— Отримати загальну кількість влучень у кеш
-   [APCUIterator::getTotalSize](apcuiterator.gettotalsize.md) \- Загальний розмір кешу
-   [APCUIterator::key](apcuiterator.key.md) \- Отримати ключ ітератора
-   [APCUIterator::next](apcuiterator.next.md)— Переміщує курсор на наступний елемент
-   [APCUIterator::rewind](apcuiterator.rewind.md) \- Перемотування ітератора
-   [APCUIterator::valid](apcuiterator.valid.md)— Перевіряє, чи поточна позиція ітератора коректна.

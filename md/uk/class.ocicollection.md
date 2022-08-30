Клас OCICollection

-   [« ociunregistertafcallback](function.oci-unregister-taf-callback.html)
    
-   [OCICollection::append »](ocicollection.append.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8](book.oci8.html)
    
-   Клас OCICollection
    

# Клас OCICollection

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

## Вступ

Функціонал колекцій OCI8

> **Зауваження**
> 
> Клас **OCI-Collection** був перейменований на **OCICollection** у PHP 8 OCI8 3.0.0 відповідно до стандартів іменування PHP.

## Огляд класів

```classsynopsis

     
    

    
     
      class OCICollection
     
     {

    /* Методы */
    
   public append(string $value): bool
public assign(OCICollection $from): bool
public assignElem(int $index, string $value): bool
public free(): bool
public getElem(int $index): string|float|null|false
public max(): int|false
public size(): int|false
public trim(int $num): bool

   }
```

## Зміст

-   [OCICollection::append](ocicollection.append.html) — Додає елемент у колекцію
-   [OCICollection::assign](ocicollection.assign.html) — Надає колекції значення іншої, вже існуючої колекції
-   [OCICollection::assignElem](ocicollection.assignelem.html) — Надає значення елементу колекції
-   [OCICollection::free](ocicollection.free.html) — Звільняє ресурси, які займає об'єкт колекції.
-   [OCICollection::getElem](ocicollection.getelem.html) — Повертає значення елемента
-   [OCICollection::max](ocicollection.max.html) — Повертає максимальну кількість елементів у колекції
-   [OCICollection::size](ocicollection.size.html) — Повертає кількість елементів у колекції
-   [OCICollection::trim](ocicollection.trim.html) — Відсікає елементи з кінця колекції
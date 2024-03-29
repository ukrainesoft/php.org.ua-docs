---
navigation:
  - function.oci-unregister-taf-callback.md: « oci\_unregister\_taf\_callback
  - ocicollection.append.md: 'OCICollection::append »'
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: Клас OCICollection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас OCICollection

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

## Вступ

Функціонал колекцій OCI8

> **Зауваження** :
> 
> Класс**OCI-Collection** був перейменований на **OCICollection**в PHP 8 OCI8 3.0.0 в соответствии со стандартами именования PHP.

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

-   [OCICollection::append](ocicollection.append.md)— Додає елемент у колекцію
-   [OCICollection::assign](ocicollection.assign.md)— Надає колекції значення іншої, вже існуючої колекції
-   [OCICollection::assignElem](ocicollection.assignelem.md)— Надає значення елементу колекції
-   [OCICollection::free](ocicollection.free.md)— Звільняє ресурси, які займає об'єкт колекції.
-   [OCICollection::getElem](ocicollection.getelem.md)— Повертає значення елемента
-   [OCICollection::max](ocicollection.max.md)— Повертає максимальну кількість елементів у колекції
-   [OCICollection::size](ocicollection.size.md)— Повертає кількість елементів у колекції
-   [OCICollection::trim](ocicollection.trim.md)— Відсікає елементи з кінця колекції

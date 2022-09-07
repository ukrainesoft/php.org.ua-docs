---
navigation:
  - mysql-xdevapi-collectionfind.sort.md: '« CollectionFind::sort'
  - mysql-xdevapi-collectionmodify.arrayappend.md: 'CollectionModify::arrayAppend »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Клас CollectionModify
---
# Клас CollectionModify

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\CollectionModify
     

     implements 
       mysql_xdevapi\Executable,  mysql_xdevapi\CrudOperationBindable,  mysql_xdevapi\CrudOperationLimitable,  mysql_xdevapi\CrudOperationSkippable,  mysql_xdevapi\CrudOperationSortable {


    /* Методы */
    
   public arrayAppend(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
public arrayInsert(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
public bind(array $placeholder_values): mysql_xdevapi\CollectionModify
public execute(): mysql_xdevapi\Result
public limit(int $rows): mysql_xdevapi\CollectionModify
public patch(string $document): mysql_xdevapi\CollectionModify
public replace(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
public set(string $collection_field, string $expression_or_literal): mysql_xdevapi\CollectionModify
public skip(int $position): mysql_xdevapi\CollectionModify
public sort(string $sort_expr): mysql_xdevapi\CollectionModify
public unset(array $fields): mysql_xdevapi\CollectionModify

   }
```

## Зміст

-   [CollectionModify::arrayAppend](mysql-xdevapi-collectionmodify.arrayappend.md) — Додає елемент у поле масиву
-   [CollectionModify::arrayInsert](mysql-xdevapi-collectionmodify.arrayinsert.md) — Додає елемент у поле масиву
-   [CollectionModify::bind](mysql-xdevapi-collectionmodify.bind.md) — Прив'язує значення до заповнювача запиту
-   [CollectionModify::construct](mysql-xdevapi-collectionmodify.construct.md) - Конструктор класу CollectionModify
-   [CollectionModify::execute](mysql-xdevapi-collectionmodify.execute.md) - Виконує операцію зміни
-   [CollectionModify::limit](mysql-xdevapi-collectionmodify.limit.md) — Обмежує кількість документів, що змінюються.
-   [CollectionModify::patch](mysql-xdevapi-collectionmodify.patch.md) - Виправляє документ
-   [CollectionModify::replace](mysql-xdevapi-collectionmodify.replace.md) - Замінює поле документа
-   [CollectionModify::set](mysql-xdevapi-collectionmodify.set.md) - Встановлює атрибут документа
-   [CollectionModify::skip](mysql-xdevapi-collectionmodify.skip.md) - Пропускає елементи
-   [CollectionModify::sort](mysql-xdevapi-collectionmodify.sort.md) - Встановлює критерії сортування
-   [CollectionModify::unset](mysql-xdevapi-collectionmodify.unset.md) — скидає значення полів документа

Клас CollectionModify

-   [« CollectionFind::sort](mysql-xdevapi-collectionfind.sort.html)
    
-   [CollectionModify::arrayAppend »](mysql-xdevapi-collectionmodify.arrayappend.html)
    
-   [PHP Manual](index.md)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас CollectionModify
    

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

-   [CollectionModify::arrayAppend](mysql-xdevapi-collectionmodify.arrayappend.html) — Додає елемент у поле масиву
-   [CollectionModify::arrayInsert](mysql-xdevapi-collectionmodify.arrayinsert.html) — Додає елемент у поле масиву
-   [CollectionModify::bind](mysql-xdevapi-collectionmodify.bind.html) — Прив'язує значення до заповнювача запиту
-   [CollectionModify::construct](mysql-xdevapi-collectionmodify.construct.html) - Конструктор класу CollectionModify
-   [CollectionModify::execute](mysql-xdevapi-collectionmodify.execute.html) - Виконує операцію зміни
-   [CollectionModify::limit](mysql-xdevapi-collectionmodify.limit.html) — Обмежує кількість документів, що змінюються.
-   [CollectionModify::patch](mysql-xdevapi-collectionmodify.patch.html) - Виправляє документ
-   [CollectionModify::replace](mysql-xdevapi-collectionmodify.replace.html) - Замінює поле документа
-   [CollectionModify::set](mysql-xdevapi-collectionmodify.set.html) - Встановлює атрибут документа
-   [CollectionModify::skip](mysql-xdevapi-collectionmodify.skip.html) - Пропускає елементи
-   [CollectionModify::sort](mysql-xdevapi-collectionmodify.sort.html) - Встановлює критерії сортування
-   [CollectionModify::unset](mysql-xdevapi-collectionmodify.unset.html) — скидає значення полів документа
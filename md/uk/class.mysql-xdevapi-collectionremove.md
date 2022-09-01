---
navigation:
  - mysql-xdevapi-collectionmodify.unset.html: '« CollectionModify::unset'
  - mysql-xdevapi-collectionremove.bind.html: 'CollectionRemove::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас CollectionRemove
---
# Клас CollectionRemove

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\CollectionRemove
     

     implements 
       mysql_xdevapi\Executable,  mysql_xdevapi\CrudOperationBindable,  mysql_xdevapi\CrudOperationLimitable,  mysql_xdevapi\CrudOperationSortable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\CollectionRemove
public execute(): mysql_xdevapi\Result
public limit(int $rows): mysql_xdevapi\CollectionRemove
public sort(string $sort_expr): mysql_xdevapi\CollectionRemove

   }
```

## Зміст

-   [CollectionRemove::bind](mysql-xdevapi-collectionremove.bind.md) — Прив'язує значення до заповнювача
-   [CollectionRemove::construct](mysql-xdevapi-collectionremove.construct.md) - Конструктор класу CollectionRemove
-   [CollectionRemove::execute](mysql-xdevapi-collectionremove.execute.md) - Виконує операцію видалення
-   [CollectionRemove::limit](mysql-xdevapi-collectionremove.limit.md) — Обмежує кількість документів для видалення
-   [CollectionRemove::sort](mysql-xdevapi-collectionremove.sort.md) - Встановлює критерії сортування

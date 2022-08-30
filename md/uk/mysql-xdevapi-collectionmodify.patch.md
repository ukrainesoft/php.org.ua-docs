Виправляє документ

-   [« CollectionModify::limit](mysql-xdevapi-collectionmodify.limit.html)
    
-   [CollectionModify::replace »](mysql-xdevapi-collectionmodify.replace.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiCollectionModify](class.mysql-xdevapi-collectionmodify.html)
    
-   Виправляє документ
    

# CollectionModify::patch

(No version information available, might only be in Git)

CollectionModify::patch — Виправляє документ

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::patch(string $document): mysql_xdevapi\CollectionModify
```

Приймає об'єкт виправлення та застосовує його до одного або кількох документів та може оновлювати декілька властивостей документа.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`document`

Документ із властивостями, які застосовуються до відповідних документів.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollectionModify::patch()****

```php
<?php

$res = $coll->modify('"Programmatore" IN job')->patch('{"Hobby" : "Programmare"}')->execute();

?>
```
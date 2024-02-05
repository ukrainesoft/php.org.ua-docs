---
navigation:
  - mysql-xdevapi-collectionmodify.limit.md: '« CollectionModify::limit'
  - mysql-xdevapi-collectionmodify.replace.md: 'CollectionModify::replace »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collectionmodify.md: mysql\_xdevapi\\CollectionModify
title: 'CollectionModify::patch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CollectionModify::patch

(No version information available, might only be in Git)

CollectionModify::patch — Виправляє документ

### Опис

```methodsynopsis
public mysql_xdevapi\CollectionModify::patch(string $document): mysql_xdevapi\CollectionModify
```

Приймає об'єкт виправлення та застосовує його до одного або кількох документів і може оновлювати кілька властивостей документа.

### Список параметрів

`document`

Документ із властивостями, які застосовуються до відповідних документів.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\CollectionModify::patch()\*\*\*\*

```php
<?php

$res = $coll->modify('"Programmatore" IN job')->patch('{"Hobby" : "Programmare"}')->execute();

?>
```

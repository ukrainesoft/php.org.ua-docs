Конструктор класу

-   [« SolrDisMaxQuery::addUserField](solrdismaxquery.adduserfield.html)
    
-   [SolrDisMaxQuery::removeBigramPhraseField »](solrdismaxquery.removebigramphrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Конструктор класу
    

# SolrDisMaxQuery::construct

(No version information available, might only be in Git)

SolrDisMaxQuery::construct - Конструктор класу

### Опис

public **SolrDisMaxQuery::construct**(string `$q`

Конструктор класу ініціалізує об'єкт та встановлює параметр q, якщо він вказаний

### Список параметрів

`q`

Пошуковий запит (параметр q)

### Значення, що повертаються

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.html) у разі передачі неправильного параметра.

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::construct()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
echo $dismaxQuery;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=edismax
```
Перемикає QueryParser на EDisMax

-   [« SolrDisMaxQuery::useDisMaxQueryParser](solrdismaxquery.usedismaxqueryparser.md)
    
-   [SolrCollapseFunction »](class.solrcollapsefunction.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Перемикає QueryParser на EDisMax
    

# SolrDisMaxQuery::useEDisMaxQueryParser

(No version information available, might only be in Git)

SolrDisMaxQuery::useEDisMaxQueryParser — Перемикає QueryParser на EDisMax

### Опис

```methodsynopsis
public SolrDisMaxQuery::useEDisMaxQueryParser(): SolrDisMaxQuery
```

Перемикає QueryParser на EDisMax. За замовчуванням будівельник запитів використовує edismax, якщо він був переключений за допомогою [SolrDisMaxQuery::useDisMaxQueryParser()](solrdismaxquery.usedismaxqueryparser.md), його можна переключити за допомогою цього методу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::useEDisMaxQueryParser()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->useEDisMaxQueryParser();
echo $dismaxQuery;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=edismax
```
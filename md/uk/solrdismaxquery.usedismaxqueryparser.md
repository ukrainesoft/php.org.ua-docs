Перемикає QueryParser на DisMax Query Parser

-   [« SolrDisMaxQuery::setUserFields](solrdismaxquery.setuserfields.md)
    
-   [SolrDisMaxQuery::useEDisMaxQueryParser »](solrdismaxquery.useedismaxqueryparser.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Перемикає QueryParser на DisMax Query Parser
    

# SolrDisMaxQuery::useDisMaxQueryParser

(No version information available, might only be in Git)

SolrDisMaxQuery::useDisMaxQueryParser — Перемикає QueryParser на DisMax Query Parser

### Опис

```methodsynopsis
public SolrDisMaxQuery::useDisMaxQueryParser(): SolrDisMaxQuery
```

Перемикає QueryParser на DisMax Query Parser

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::useDisMaxQueryParser()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->useDisMaxQueryParser();
echo $dismaxQuery;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=dismax
```

### Дивіться також

-   **SolrDisMaxQuery::useDisMaxQueryParser()**
---
navigation:
  - solrdismaxquery.setuserfields.md: '« SolrDisMaxQuery::setUserFields'
  - solrdismaxquery.useedismaxqueryparser.md: 'SolrDisMaxQuery::useEDisMaxQueryParser »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::useDisMaxQueryParser'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Приклад #1 Приклад використання** SolrDisMaxQuery::useDisMaxQueryParser()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->useDisMaxQueryParser();
echo $dismaxQuery;
?>
```

Висновок наведеного прикладу буде схожим на:

```
defType=dismax
```

### Дивіться також

-   **SolrDisMaxQuery::useDisMaxQueryParser()**

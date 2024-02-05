---
navigation:
  - solrdismaxquery.usedismaxqueryparser.md: '« SolrDisMaxQuery::useDisMaxQueryParser'
  - class.solrcollapsefunction.md: SolrCollapseFunction »
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::useEDisMaxQueryParser'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Приклад #1 Приклад використання** SolrDisMaxQuery::useEDisMaxQueryParser()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->useEDisMaxQueryParser();
echo $dismaxQuery;

?>
```

Висновок наведеного прикладу буде схожим на:

```
defType=edismax
```

---
navigation:
  - solrdismaxquery.setbigramphrasefields.md: '« SolrDisMaxQuery::setBigramPhraseFields'
  - solrdismaxquery.setboostfunction.md: 'SolrDisMaxQuery::setBoostFunction »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setBigramPhraseSlop'
---
# SolrDisMaxQuery::setBigramPhraseSlop

(No version information available, might only be in Git)

SolrDisMaxQuery::setBigramPhraseSlop — Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setBigramPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення біграми фрази (параметр ps2). Коефіцієнт відхилення за промовчанням для полів біграми фрази.

### Список параметрів

`slop`

Коефіцієнт відхилення.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setBigramPhraseSlop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$dismaxQuery->setBigramPhraseSlop(5);
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&ps2=5
```

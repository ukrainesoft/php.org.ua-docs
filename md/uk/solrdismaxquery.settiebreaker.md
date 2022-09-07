---
navigation:
  - solrdismaxquery.setqueryphraseslop.md: '« SolrDisMaxQuery::setQueryPhraseSlop'
  - solrdismaxquery.settrigramphrasefields.md: 'SolrDisMaxQuery::setTrigramPhraseFields »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'Solr DisMax Query::set TieBreaker'
---
# Solr DisMax Query::set TieBreaker

(No version information available, might only be in Git)

SolrDisMaxQuery::setTieBreaker — Встановлює параметр Tie Breaker (параметр tie)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTieBreaker(string $tieBreaker): SolrDisMaxQuery
```

Встановлює параметр Tie Breaker (Параметр tie).

### Список параметрів

`tieBreaker`

Параметр *tie* вказує значення з плаваючою точкою (яке має бути набагато менше 1) для використання як вирішення конфліктів у запитах DisMax.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set TieBreaker()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setTieBreaker(0.1);

echo $dismaxQuery;
?>
```

Результат виконання цього прикладу:

```
defType=edismax&tie=0.1
```

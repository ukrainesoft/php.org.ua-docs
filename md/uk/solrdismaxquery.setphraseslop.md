---
navigation:
  - solrdismaxquery.setphrasefields.md: '« SolrDisMaxQuery::setPhraseFields'
  - solrdismaxquery.setqueryalt.md: 'SolrDisMaxQuery::setQueryAlt »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'Solr DisMax Query::set Phrase Slop'
---
# Solr DisMax Query::set Phrase Slop

(No version information available, might only be in Git)

SolrDisMaxQuery::setPhraseSlop — Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення за замовчуванням фразових запитів, побудованих з полями "pf", "pf2" and/or "pf3" (впливає на посилення). Параметр "ps".

### Список параметрів

`slop`

Коефіцієнт відхилення за замовчуванням.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set Phrase Slop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$dismaxQuery->setPhraseSlop(4);
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=edismax&ps=4
```

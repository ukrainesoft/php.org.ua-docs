---
navigation:
  - solrdismaxquery.setphrasefields.md: '« SolrDisMaxQuery::setPhraseFields'
  - solrdismaxquery.setqueryalt.md: 'SolrDisMaxQuery::setQueryAlt »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setPhraseSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setPhraseSlop

(No version information available, might only be in Git)

SolrDisMaxQuery::setPhraseSlop — Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення за промовчанням для фразових запитів, побудованих з полями "pf", "pf2" та/or "pf3" (впливає на посилення). Параметр "ps".

### Список параметрів

`slop`

Коефіцієнт відхилення за замовчуванням.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Пример #1 Пример использования**SolrDisMaxQuery::setPhraseSlop()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$dismaxQuery->setPhraseSlop(4);
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання наведеного прикладу:

```
q=lucene&defType=edismax&ps=4
```

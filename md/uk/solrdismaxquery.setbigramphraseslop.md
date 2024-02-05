---
navigation:
  - solrdismaxquery.setbigramphrasefields.md: '« SolrDisMaxQuery::setBigramPhraseFields'
  - solrdismaxquery.setboostfunction.md: 'SolrDisMaxQuery::setBoostFunction »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setBigramPhraseSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**SolrDisMaxQuery::setBigramPhraseSlop()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$dismaxQuery->setBigramPhraseSlop(5);
echo $dismaxQuery.PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&ps2=5
```

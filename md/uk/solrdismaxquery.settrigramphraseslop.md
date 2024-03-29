---
navigation:
  - solrdismaxquery.settrigramphrasefields.md: '« SolrDisMaxQuery::setTrigramPhraseFields'
  - solrdismaxquery.setuserfields.md: 'SolrDisMaxQuery::setUserFields »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setTrigramPhraseSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setTrigramPhraseSlop

(No version information available, might only be in Git)

SolrDisMaxQuery::setTrigramPhraseSlop — Встановлює коефіцієнт відхилення триграми фрази (параметр ps3)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTrigramPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення триграм фрази (параметр ps3).

### Список параметрів

`slop`

Коефіцієнт відхилення.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::setTrigramPhraseSlop()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setTrigramPhraseSlop(2);
echo $dismaxQuery.PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&ps3=2
```

### Дивіться також

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.md) \- Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::removeTrigramPhraseField()](solrdismaxquery.removetrigramphrasefield.md) \- Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.md) \- Безпосередньо встановлює поля триграм фрази (параметр pf3)

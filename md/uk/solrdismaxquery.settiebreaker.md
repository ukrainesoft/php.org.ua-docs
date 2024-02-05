---
navigation:
  - solrdismaxquery.setqueryphraseslop.md: '« SolrDisMaxQuery::setQueryPhraseSlop'
  - solrdismaxquery.settrigramphrasefields.md: 'SolrDisMaxQuery::setTrigramPhraseFields »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setTieBreaker'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setTieBreaker

(No version information available, might only be in Git)

SolrDisMaxQuery::setTieBreaker — Встановлює параметр Tie Breaker (параметр tie)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTieBreaker(string $tieBreaker): SolrDisMaxQuery
```

Встановлює параметр Tie Breaker (Параметр tie).

### Список параметрів

`tieBreaker`

Параметр*tie* вказує значення з плаваючою точкою (яке має бути набагато менше 1) для використання як вирішення конфліктів у запитах DisMax.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Пример #1 Пример использования**SolrDisMaxQuery::setTieBreaker()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setTieBreaker(0.1);

echo $dismaxQuery;
?>
```

Результат виконання наведеного прикладу:

```
defType=edismax&tie=0.1
```

---
navigation:
  - solrdismaxquery.setqueryalt.md: '« SolrDisMaxQuery::setQueryAlt'
  - solrdismaxquery.settiebreaker.md: 'SolrDisMaxQuery::setTieBreaker »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setQueryPhraseSlop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setQueryPhraseSlop

(No version information available, might only be in Git)

SolrDisMaxQuery::setQueryPhraseSlop — Визначає коефіцієнт відхилення, дозволений для фразових запитів, явно включених до рядка запиту користувача (параметр qf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setQueryPhraseSlop(string $slop): SolrDisMaxQuery
```

Визначає коефіцієнт відхилення, дозволений для фразових запитів, які явно включені в рядок запиту користувача (параметр *qf*

p align="justify"> Коефіцієнт відхилення відноситься до кількості позицій, на які необхідно перемістити один токен по відношенню до іншого токену, щоб відповідати фразі, зазначеній у запиті.

### Список параметрів

`slop`

Коефіцієнт відхилення.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Пример #1 Пример использования**SolrDisMaxQuery::setQueryPhraseSlop()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setQueryPhraseSlop(3);
echo $dismaxQuery;
?>
```

Висновок наведеного прикладу буде схожим на:

```
defType=edismax&qs=3
```

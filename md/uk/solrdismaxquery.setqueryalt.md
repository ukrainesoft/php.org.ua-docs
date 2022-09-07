---
navigation:
  - solrdismaxquery.setphraseslop.md: '« SolrDisMaxQuery::setPhraseSlop'
  - solrdismaxquery.setqueryphraseslop.md: 'SolrDisMaxQuery::setQueryPhraseSlop »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setQueryAlt'
---
# SolrDisMaxQuery::setQueryAlt

(No version information available, might only be in Git)

SolrDisMaxQuery::setQueryAlt — Встановлює альтернативний запит (параметр q.alt)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setQueryAlt(string $q): SolrDisMaxQuery
```

Встановлює альтернативний запит (параметр q.alt).

Коли основний параметр *до* не вказаний чи порожній. Використовується параметр *q.alt*

### Список параметрів

`q`

Рядок запиту.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setQueryAlt()****

```php
<?php

$dismaxQuery = new DisMaxQuery();
$dismaxQuery->setQueryAlt('*:*');

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=edismax&q.alt=*:*&q=
```

---
navigation:
  - solrdismaxquery.adduserfield.md: '« SolrDisMaxQuery::addUserField'
  - solrdismaxquery.removebigramphrasefield.md: 'SolrDisMaxQuery::removeBigramPhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::\_\_construct

(No version information available, might only be in Git)

SolrDisMaxQuery::\_\_construct - Конструктор класу

### Опис

public **SolrDisMaxQuery::\_\_construct**(string`$q`

Конструктор класу ініціалізує об'єкт та встановлює параметр q, якщо він вказаний

### Список параметрів

`q`

Пошуковий запит (параметр q)

### Значення, що повертаються

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md)в случае передачи неверного параметра.

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::\_\_construct()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
echo $dismaxQuery;

?>
```

Результат виконання наведеного прикладу:

```
q=lucene&defType=edismax
```

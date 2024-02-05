---
navigation:
  - solrdismaxquery.addphrasefield.md: '« SolrDisMaxQuery::addPhraseField'
  - solrdismaxquery.addtrigramphrasefield.md: 'SolrDisMaxQuery::addTrigramPhraseField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::addQueryField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::addQueryField

(No version information available, might only be in Git)

SolrDisMaxQuery::addQueryField — Додає поле запиту з необов'язковим підвищенням (параметр qf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addQueryField(string $field, string $boost = ?): SolrDisMaxQuery
```

Додає поле запиту із необов'язковим підвищенням

### Список параметрів

`field`

Ім'я поля

`boost`

Підвищення значення. Додає документи із відповідними виразами.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::addQueryField()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addQueryField("location", 4)
    ->addQueryField("price")
    ->addQueryField("sku")
    ->addQueryField("title",3.4)
;
echo $dismaxQuery;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&qf=location^4 price sku title^3.4
```

### Дивіться також

-   [SolrDisMaxQuery::removeQueryField()](solrdismaxquery.removequeryfield.md) \- Видаляє поле запиту (параметр qf)

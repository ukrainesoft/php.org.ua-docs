Додає поле запиту з необов'язковим збільшенням (параметр qf)

-   [« SolrDisMaxQuery::addPhraseField](solrdismaxquery.addphrasefield.md)
    
-   [SolrDisMaxQuery::addTrigramPhraseField »](solrdismaxquery.addtrigramphrasefield.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Додає поле запиту з необов'язковим збільшенням (параметр qf)
    

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

**Приклад #1 Приклад використання **SolrDisMaxQuery::addQueryField()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addQueryField("location", 4)
    ->addQueryField("price")
    ->addQueryField("sku")
    ->addQueryField("title",3.4)
;
echo $dismaxQuery;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&qf=location^4 price sku title^3.4
```

### Дивіться також

-   [SolrDisMaxQuery::removeQueryField()](solrdismaxquery.removequeryfield.md) - Видаляє поле запиту (параметр qf)
Додає поле запиту з необов'язковим збільшенням (параметр qf)

-   [« SolrDisMaxQuery::addPhraseField](solrdismaxquery.addphrasefield.html)
    
-   [SolrDisMaxQuery::addTrigramPhraseField »](solrdismaxquery.addtrigramphrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
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

[SolrDisMaxQuery](class.solrdismaxquery.html)

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

-   [SolrDisMaxQuery::removeQueryField()](solrdismaxquery.removequeryfield.html) - Видаляє поле запиту (параметр qf)
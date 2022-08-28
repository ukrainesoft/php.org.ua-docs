Додає поле фрази (параметр pf)

-   [« SolrDisMaxQuery::addBoostQuery](solrdismaxquery.addboostquery.html)
    
-   [SolrDisMaxQuery::addQueryField »](solrdismaxquery.addqueryfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Додає поле фрази (параметр pf)
    

# Solr DisMax Query::add Phrase Field

(No version information available, might only be in Git)

SolrDisMaxQuery::addPhraseField — Додає поле фрази (параметр pf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
```

Додає поле фрази (параметр pf)

### Список параметрів

`field`

field name

`boost`

`slop`

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::add Phrase Field()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addPhraseField('cat', 3, 1)
    ->addPhraseField('third', 4, 2)
    ->addPhraseField('source', 55)
;
echo $dismaxQuery;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf=cat~1^3 third~2^4 source^55
```

### Дивіться також

-   [SolrDisMaxQuery::removePhraseField()](solrdismaxquery.removephrasefield.html) - Видаляє поле фрази (параметра)
-   [SolrDisMaxQuery::setPhraseFields()](solrdismaxquery.setphrasefields.html) - Встановлює поля фрази та їх посилення (і відхилення) за допомогою параметра pf2
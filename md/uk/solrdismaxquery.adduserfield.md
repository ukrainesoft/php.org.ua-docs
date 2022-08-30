Додає поле до параметра поля користувача (uf)

-   [« SolrDisMaxQuery::addTrigramPhraseField](solrdismaxquery.addtrigramphrasefield.md)
    
-   [SolrDisMaxQuery::construct »](solrdismaxquery.construct.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Додає поле до параметра поля користувача (uf)
    

# Solr DisMax Query::add User Field

(No version information available, might only be in Git)

SolrDisMaxQuery::addUserField — Додає поле до параметра поля користувача (uf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addUserField(string $field): SolrDisMaxQuery
```

Додає поле до параметра поля користувача (uf)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::add User Field()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addUserField('cat')
->addUserField('text')
->addUserField('*_dt');

echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&uf=cat text *_dt
```

### Дивіться також

-   [SolrDisMaxQuery::removeUserField()](solrdismaxquery.removeuserfield.md) - Видаляє поле з параметра користувацьких полів (uf)
-   [SolrDisMaxQuery::setUserFields()](solrdismaxquery.setuserfields.md) - Встановлює параметр полів користувача (uf)
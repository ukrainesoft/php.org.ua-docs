Встановлює параметр полів користувача (uf)

-   [« SolrDisMaxQuery::setTrigramPhraseSlop](solrdismaxquery.settrigramphraseslop.html)
    
-   [SolrDisMaxQuery::useDisMaxQueryParser »](solrdismaxquery.usedismaxqueryparser.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Встановлює параметр полів користувача (uf)
    

# Solr DisMax Query::set User Fields

(No version information available, might only be in Git)

SolrDisMaxQuery::setUserFields — Встановлює параметр для користувача полів (uf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setUserFields(string $fields): SolrDisMaxQuery
```

Встановлює параметр полів користувача (uf)

Поля користувача: вказує, які поля схеми кінцевий користувач може запитувати.

### Список параметрів

`fields`

Імена полів, вказані через пропуск

Параметр підтримує знаки підстановки.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set User Fields()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setUserFields('field1 field2 *_txt');
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&uf=field1 field2 *_txt
```

### Дивіться також

-   [SolrDisMaxQuery::addUserField()](solrdismaxquery.adduserfield.html) - Додає поле до параметра користувача полів (uf)
-   [SolrDisMaxQuery::removeUserField()](solrdismaxquery.removeuserfield.html) - Видаляє поле з параметра користувацьких полів (uf)
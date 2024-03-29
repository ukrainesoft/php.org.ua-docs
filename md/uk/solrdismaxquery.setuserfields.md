---
navigation:
  - solrdismaxquery.settrigramphraseslop.md: '« SolrDisMaxQuery::setTrigramPhraseSlop'
  - solrdismaxquery.usedismaxqueryparser.md: 'SolrDisMaxQuery::useDisMaxQueryParser »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setUserFields'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setUserFields

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

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::setUserFields()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setUserFields('field1 field2 *_txt');
echo $dismaxQuery.PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&uf=field1 field2 *_txt
```

### Дивіться також

-   [SolrDisMaxQuery::addUserField()](solrdismaxquery.adduserfield.md) \- Додає поле до параметра користувача полів (uf)
-   [SolrDisMaxQuery::removeUserField()](solrdismaxquery.removeuserfield.md) \- Видаляє поле з параметра користувацьких полів (uf)

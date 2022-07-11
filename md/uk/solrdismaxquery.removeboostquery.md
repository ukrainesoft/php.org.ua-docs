- [« SolrDisMaxQuery::removeBigramPhraseField](solrdismaxquery.removebigramphrasefield.md)
- [SolrDisMaxQuery::removePhraseField »](solrdismaxquery.removephrasefield.md)

- [PHP Manual](index.md)
- [SolrDisMaxQuery](class.solrdismaxquery.md)
- Видаляє часткове підвищення запиту на ім'я поля (bq)

# SolrDisMaxQuery::removeBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::removeBoostQuery — Видаляє часткове підвищення запиту
на ім'я поля (bq)

### Опис

public **SolrDisMaxQuery::removeBoostQuery**(string `$field`):
[SolrDisMaxQuery](class.solrdismaxquery.md)

Видаляє частковий запит на підвищення з існуючого запиту, лише якщо
було виконано
[SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md).

### Список параметрів

`field`
Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання
**SolrDisMaxQuery::removeBoostQuery()****

`<?php$dismaxQuery = new SolrDisMaxQuery("lucene");$dismaxQuery   ->addBoostQuery('cat', 'electronics', 5.1)    ->addBoostQuery('_ ;// тепер видалите частину запиту з полем 'cat'$dismaxQuery->removeBoostQuery('cat');echo $dismaxQuery . PHP_EOL;?> `

Результатом виконання цього прикладу буде щось подібне:

q=lucene&defType=edismax&bq=cat:electronics^5.1 cat:hard drive
q=lucene&defType=edismax&bq=cat:hard drive

### Дивіться також

- [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.md) -
Додає поле підвищення запиту зі значенням та необов'язковим
посиленням (параметр bq)
- [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.md) -
Безпосередньо встановлює параметр запиту на посилення (bq)

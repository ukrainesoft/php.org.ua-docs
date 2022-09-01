---
navigation:
  - solrquery.addgroupquery.html: '« SolrQuery::addGroupQuery'
  - solrquery.addhighlightfield.html: 'SolrQuery::addHighlightField »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
title: 'SolrQuery::addGroupSortField'
---
# SolrQuery::addGroupSortField

(PECL solr> = 2.2.0)

SolrQuery::addGroupSortField — Додає поле сортування групи (параметр group.sort)

### Опис

```methodsynopsis
public SolrQuery::addGroupSortField(string $field, int $order = ?): SolrQuery
```

Дозволяє сортувати групові документи за допомогою поля сортування групи (параметр group.sort).

### Список параметрів

`field`

Назва поля

`order`

Напрямок сортування ASC/DESC, використовуйте константи SolrQuery::ORDER

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **SolrQuery::addGroupSortField()****

```php
<?php

$solrQuery = new SolrQuery('*:*');
$solrQuery
    ->setGroup(true)
    ->addGroupSortField('price', SolrQuery::ORDER_ASC);

echo $solrQuery;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=*:*&group=true&group.sort=price asc
```

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.html) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.html) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.html) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.html) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.html) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.html) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.html) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.html) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.html) - Включає кешування для угруповання результатів

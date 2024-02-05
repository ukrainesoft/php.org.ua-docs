---
navigation:
  - solrquery.setfacetsort.md: '« SolrQuery::setFacetSort'
  - solrquery.setgroupcachepercent.md: 'SolrQuery::setGroupCachePercent »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setGroup'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setGroup

(PECL solr >= 2.2.0)

SolrQuery::setGroup — Вмикає/вимикає групування результатів (параметр group)

### Опис

```methodsynopsis
public SolrQuery::setGroup(bool $value): SolrQuery
```

Включає/вимикає групування результатів (параметр group)

### Список параметрів

`value`

### Значення, що повертаються

### Дивіться також

-   [SolrQuery::getGroup()](solrquery.getgroup.md) \- Повертає true, якщо угруповання увімкнено
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.md) \- Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.md) \- Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.md) \- Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.md) \- Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.md) \- Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.md) \- Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.md) \- Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.md) \- Якщо true, результат першої команди групування полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.md) \- Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.md) \- Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.md) \- Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.md) \- Включає кешування для угруповання результатів

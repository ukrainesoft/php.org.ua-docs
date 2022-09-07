---
navigation:
  - solrquery.addgroupfield.md: '« SolrQuery::addGroupField'
  - solrquery.addgroupquery.md: 'SolrQuery::addGroupQuery »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addGroupFunction'
---
# SolrQuery::addGroupFunction

(PECL solr> = 2.2.0)

SolrQuery::addGroupFunction — Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)

### Опис

```methodsynopsis
public SolrQuery::addGroupFunction(string $value): SolrQuery
```

Додає функцію групування (параметр group.func) Дозволяє групувати результати на основі унікальних значень запиту функції.

### Список параметрів

`value`

### Значення, що повертаються

[SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.md) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.md) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.md) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.md) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.md) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.md) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.md) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.md) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.md) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.md) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.md) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.md) - Включає кешування для угруповання результатів

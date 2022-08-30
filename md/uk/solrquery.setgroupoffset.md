Встановлює параметр group.offset

-   [« SolrQuery::setGroupNGroups](solrquery.setgroupngroups.md)
    
-   [SolrQuery::setGroupTruncate »](solrquery.setgrouptruncate.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Встановлює параметр group.offset
    

# SolrQuery::setGroupOffset

(PECL solr> = 2.2.0)

SolrQuery::setGroupOffset — Встановлює параметр group.offset

### Опис

```methodsynopsis
public SolrQuery::setGroupOffset(int $value): SolrQuery
```

Встановлює параметр group.offset

### Список параметрів

`value`

### Значення, що повертаються

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.md) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.md) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.md) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.md) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.md) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.md) - Встановлює параметр group.facet
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.md) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.md) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.md) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.md) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.md) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.md) - Включає кешування для угруповання результатів
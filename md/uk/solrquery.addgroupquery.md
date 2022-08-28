Дозволяє групувати документи, що відповідають цьому запиту

-   [« SolrQuery::addGroupFunction](solrquery.addgroupfunction.html)
    
-   [SolrQuery::addGroupSortField »](solrquery.addgroupsortfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Дозволяє групувати документи, що відповідають цьому запиту
    

# SolrQuery::addGroupQuery

(PECL solr> = 2.2.0)

SolrQuery::addGroupQuery — Дозволяє групувати документи, які відповідають цьому запиту

### Опис

```methodsynopsis
public SolrQuery::addGroupQuery(string $value): SolrQuery
```

Дозволяє групувати документи, які відповідають цьому запиту. Додає запит до параметра group.query

### Список параметрів

`value`

### Значення, що повертаються

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.html) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.html) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.html) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.html) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.html) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.html) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.html) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.html) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.html) - Включає кешування для угруповання результатів
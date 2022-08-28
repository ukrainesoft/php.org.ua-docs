Якщо true, результат першої команди групування полів використовується як основний список результатів у відповіді з використанням group.format=simple

-   [« SolrQuery::setGroupLimit](solrquery.setgrouplimit.html)
    
-   [SolrQuery::setGroupNGroups »](solrquery.setgroupngroups.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Якщо true, результат першої команди групування полів використовується як основний список результатів у відповіді з використанням group.format=simple
    

# SolrQuery::setGroupMain

(PECL solr> = 2.2.0)

SolrQuery::setGroupMain — Якщо true, результат першої команди групування полів використовується як основний список результатів у відповіді з використанням group.format=simple

### Опис

```methodsynopsis
public SolrQuery::setGroupMain(string $value): SolrQuery
```

Якщо **`true`**, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням `group.format=simple`

### Список параметрів

`value`

Якщо **`true`**, результат першої команди угруповання полів використовується як основний список результатів у відповіді.

### Значення, що повертаються

Повертає екземпляр [SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.html) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.html) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.html) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.html) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.html) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   **SolrQuery::setGroupMain()**
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.html) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.html) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.html) - Включає кешування для угруповання результатів
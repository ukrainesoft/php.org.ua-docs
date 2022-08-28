Якщо true, підрахунок фасетів базується на найбільш релевантному документі кожної групи, що відповідає запиту

-   [« SolrQuery::setGroupOffset](solrquery.setgroupoffset.html)
    
-   [SolrQuery::setHighlight »](solrquery.sethighlight.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Якщо true, підрахунок фасетів базується на найбільш релевантному документі кожної групи, що відповідає запиту
    

# SolrQuery::setGroupTruncate

(PECL solr> = 2.2.0)

SolrQuery::setGroupTruncate — Якщо true, підрахунок фасетів базується на найбільш релевантному документі кожної групи, що відповідає запиту

### Опис

```methodsynopsis
public SolrQuery::setGroupTruncate(bool $value): SolrQuery
```

Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту. Значення сервера за промовчанням - false. Параметр group.truncate

### Список параметрів

`value`

### Значення, що повертаються

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.html) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.html) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.html) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.html) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.html) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.html) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.html) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.html) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.html) - Включає кешування для угруповання результатів
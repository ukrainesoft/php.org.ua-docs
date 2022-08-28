Дозволяє групувати результати з урахуванням унікальних значень запиту функції (параметр group.func)

-   [« SolrQuery::addGroupField](solrquery.addgroupfield.html)
    
-   [SolrQuery::addGroupQuery »](solrquery.addgroupquery.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Дозволяє групувати результати з урахуванням унікальних значень запиту функції (параметр group.func)
    

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

[SolrQuery](class.solrquery.html)

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.html) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.html) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.html) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.html) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.html) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.html) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.html) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.html) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.html) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.html) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.html) - Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.html) - Включає кешування для угруповання результатів
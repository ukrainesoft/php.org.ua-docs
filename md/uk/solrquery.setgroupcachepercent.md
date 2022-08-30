Включає кешування для угруповання результатів

-   [« SolrQuery::setGroup](solrquery.setgroup.md)
    
-   [SolrQuery::setGroupFacet »](solrquery.setgroupfacet.md)
    
-   [PHP Manual](index.md)
    
-   [SolrQuery](class.solrquery.md)
    
-   Включає кешування для угруповання результатів
    

# SolrQuery::setGroupCachePercent

(PECL solr> = 2.2.0)

SolrQuery::setGroupCachePercent — Включає кешування для групування результатів

### Опис

```methodsynopsis
public SolrQuery::setGroupCachePercent(int $percent): SolrQuery
```

Установка цього параметра числа більше 0 включає кешування для групування результатів. Група результатів виконує два пошуки; ця опція кешує другий пошук. Значення сервера за умовчанням - 0. Тестування показало, що групове кешування покращує лише час пошуку з логічними запитами, запитами з знаками підстановки і нечіткими запитами. Для простих запитів, таких як вираз або запити "порівняти все", групове кешування знижує продуктивність. Параметр group.cache.percent

### Список параметрів

`percent`

### Значення, що повертаються

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md) у разі передачі неправильного параметра.

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.md) - Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.md) - Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.md) - Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.md) - Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::addGroupSortField()](solrquery.addgroupsortfield.md) - Додає поле сортування групи (параметр group.sort)
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.md) - Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.md) - Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.md) - Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.md) - Якщо true, результат першої команди угруповання полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.md) - Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.md) - Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.md) - Встановлює формат групи, структуру результату (параметр group.format)
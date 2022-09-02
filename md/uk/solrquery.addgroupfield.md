---
navigation:
  - solrquery.addfilterquery.md: '« SolrQuery::addFilterQuery'
  - solrquery.addgroupfunction.md: 'SolrQuery::addGroupFunction »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addGroupField'
---
# SolrQuery::addGroupField

(PECL solr> = 2.2.0)

SolrQuery::addGroupField — Додає поле, яке використовуватиметься для групування результатів

### Опис

```methodsynopsis
public SolrQuery::addGroupField(string $value): SolrQuery
```

Ім'я поля, яким групуються результати. Поле має бути однозначним і індексуватися, або мати тип поля, який має джерело значення і працює в запиті функції, наприклад, ExternalFileField. Це також має бути рядкове поле, як StrField або TextField Використовує параметр group.field

### Список параметрів

`value`

Ім'я поля.

### Значення, що повертаються

Повертає екземпляр [SolrQuery](class.solrquery.md)

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.md) - Включає/вимикає групування результатів (параметр group)
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
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.md) - Включає кешування для угруповання результатів

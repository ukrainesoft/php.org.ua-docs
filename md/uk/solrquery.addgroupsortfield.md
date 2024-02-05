---
navigation:
  - solrquery.addgroupquery.md: '« SolrQuery::addGroupQuery'
  - solrquery.addhighlightfield.md: 'SolrQuery::addHighlightField »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::addGroupSortField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::addGroupSortField

(PECL solr >= 2.2.0)

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

Напрямок сортування ASC/DESC, використовуйте константи SolrQuery::ORDER\_\*

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**SolrQuery::addGroupSortField()\*\*\*\*

```php
<?php

$solrQuery = new SolrQuery('*:*');
$solrQuery
    ->setGroup(true)
    ->addGroupSortField('price', SolrQuery::ORDER_ASC);

echo $solrQuery;
?>
```

Висновок наведеного прикладу буде схожим на:

```
q=*:*&group=true&group.sort=price asc
```

### Дивіться також

-   [SolrQuery::setGroup()](solrquery.setgroup.md) \- Включає/вимикає групування результатів (параметр group)
-   [SolrQuery::addGroupField()](solrquery.addgroupfield.md) \- Додає поле, яке використовуватиметься для групування результатів
-   [SolrQuery::addGroupFunction()](solrquery.addgroupfunction.md) \- Дозволяє групувати результати на основі унікальних значень запиту функції (параметр group.func)
-   [SolrQuery::addGroupQuery()](solrquery.addgroupquery.md) \- Дозволяє групувати документи, що відповідають цьому запиту
-   [SolrQuery::setGroupFacet()](solrquery.setgroupfacet.md) \- Встановлює параметр group.facet
-   [SolrQuery::setGroupOffset()](solrquery.setgroupoffset.md) \- Встановлює параметр group.offset
-   [SolrQuery::setGroupLimit()](solrquery.setgrouplimit.md) \- Вказує кількість результатів, що повертаються для кожної групи. Значення сервера за промовчанням - 1
-   [SolrQuery::setGroupMain()](solrquery.setgroupmain.md) \- Якщо true, результат першої команди групування полів використовується як основний список результатів у відповіді з використанням group.format=simple
-   [SolrQuery::setGroupNGroups()](solrquery.setgroupngroups.md) \- Якщо true, Solr включає до результатів кількість груп, які відповідають запиту
-   [SolrQuery::setGroupTruncate()](solrquery.setgrouptruncate.md) \- Якщо true, підрахунок фасетів ґрунтується на найбільш релевантному документі кожної групи, що відповідає запиту
-   [SolrQuery::setGroupFormat()](solrquery.setgroupformat.md) \- Встановлює формат групи, структуру результату (параметр group.format)
-   [SolrQuery::setGroupCachePercent()](solrquery.setgroupcachepercent.md) \- Включає кешування для угруповання результатів

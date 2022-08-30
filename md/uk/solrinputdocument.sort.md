Сортує поля у документі

-   [« SolrInputDocument::setFieldBoost](solrinputdocument.setfieldboost.md)
    
-   [SolrInputDocument::toArray »](solrinputdocument.toarray.md)
    
-   [PHP Manual](index.md)
    
-   [SolrInputDocument](class.solrinputdocument.md)
    
-   Сортує поля у документі
    

# SolrInputDocument::sort

(PECL solr> = 0.9.2)

SolrInputDocument::sort — Сортує поля в документі

### Опис

```methodsynopsis
public SolrInputDocument::sort(int $sortOrderBy, int $sortDirection = SolrInputDocument::SORT_ASC): bool
```

Поля упорядковані відповідно до зазначених критеріїв та напряму сортування.

Поля можуть бути відсортовані за значеннями підвищення, іменами полів та кількістю значень.

Параметр $orderby повинен бути одним з :

SolrInputDocument::SORTFIELDNAME SolrInputDocument::SORTFIELDBOOSTVALUE SolrInputDocument::SORTFIELDVALUECOUNT

Напрямок сортування може бути одним з:

SolrInputDocument::SORTDEFAULT SolrInputDocument::SORTASC SolrInputDocument::SORTDESC

### Список параметрів

`sortOrderBy`

Критерій сортування

`sortDirection`

Напрямок сортування

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
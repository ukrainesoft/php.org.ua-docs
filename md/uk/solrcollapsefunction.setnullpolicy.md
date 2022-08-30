Встановлює NULL-політику

-   [« SolrCollapseFunction::setMin](solrcollapsefunction.setmin.md)
    
-   [SolrCollapseFunction::setSize »](solrcollapsefunction.setsize.md)
    
-   [PHP Manual](index.md)
    
-   [SolrCollapseFunction](class.solrcollapsefunction.md)
    
-   Встановлює NULL-політику
    

# SolrCollapseFunction::setNullPolicy

(PECL solr> = 2.2.0)

SolrCollapseFunction::setNullPolicy — Встановлює NULL-політику

### Опис

```methodsynopsis
public SolrCollapseFunction::setNullPolicy(string $nullPolicy): SolrCollapseFunction
```

Встановлює NULL-політику. Повинна бути передана одна із трьох політик, визначених як константи класу. Приймає політики ignore (ігнорування), expand (розгортання) або collapse (згортання).

### Список параметрів

`nullPolicy`

### Значення, що повертаються

[SolrCollapseFunction](class.solrcollapsefunction.md)
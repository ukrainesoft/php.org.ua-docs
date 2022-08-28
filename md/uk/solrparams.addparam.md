Додає параметр до об'єкту

-   [« SolrParams::add](solrparams.add.html)
    
-   [SolrParams::get »](solrparams.get.html)
    
-   [PHP Manual](index.html)
    
-   [SolrParams](class.solrparams.html)
    
-   Додає параметр до об'єкту
    

# SolrParams::addParam

(PECL solr> = 0.9.2)

SolrParams::addParam — Додає параметр до об'єкта

### Опис

```methodsynopsis
public SolrParams::addParam(string $name, string $value): SolrParams
```

Додавання параметра до об'єкта. Використовується для параметрів, які можна вказувати кілька разів.

### Список параметрів

`name`

Ім'я параметра

`value`

Значення параметру

### Значення, що повертаються

У разі успішного виконання повертає об'єкт SolrParam та **`false`** у разі виникнення помилки.
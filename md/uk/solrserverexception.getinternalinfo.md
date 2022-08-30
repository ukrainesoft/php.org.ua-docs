Повертає внутрішню інформацію про те, де було викинуто виняток

-   [« SolrServerException](class.solrserverexception.md)
    
-   [SolrIllegalArgumentException »](class.solrillegalargumentexception.md)
    
-   [PHP Manual](index.md)
    
-   [SolrServerException](class.solrserverexception.md)
    
-   Повертає внутрішню інформацію про те, де було викинуто виняток
    

# SolrServerException::getInternalInfo

(PECL solr >= 1.1.0, >=2.0.0)

SolrServerException::getInternalInfo — Повертає внутрішню інформацію про те, де було викинуто виняток

### Опис

```methodsynopsis
public SolrServerException::getInternalInfo(): array
```

Повертає внутрішню інформацію про те, де було викинуто виняток.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить інформацію про те, де було викинуто виняток. Використовується лише розробниками модулів для налагодження.
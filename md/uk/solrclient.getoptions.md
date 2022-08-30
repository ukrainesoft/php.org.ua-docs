Повертає внутрішні параметри клієнта

-   [« SolrClient::getDebug](solrclient.getdebug.md)
    
-   [SolrClient::optimize »](solrclient.optimize.md)
    
-   [PHP Manual](index.md)
    
-   [SolrClient](class.solrclient.md)
    
-   Повертає внутрішні параметри клієнта
    

# SolrClient::getOptions

(PECL solr> = 0.9.6)

SolrClient::getOptions — Повертає внутрішні параметри клієнта

### Опис

```methodsynopsis
public SolrClient::getOptions(): array
```

Повертає внутрішні параметри клієнта. Дуже корисно для налагодження. Значення, що повертаються, доступні тільки для читання і можуть бути встановлені тільки при створенні екземпляра об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить всі параметри об'єкта SolrClient, встановлені всередині.

### Дивіться також

-   [SolrClient::construct()](solrclient.construct.md) - Конструктор об'єкта SolrClient
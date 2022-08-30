Перевіряє статус тем

-   [« SolrClient::system](solrclient.system.md)
    
-   [SolrResponse »](class.solrresponse.md)
    
-   [PHP Manual](index.md)
    
-   [SolrClient](class.solrclient.md)
    
-   Перевіряє статус тем
    

# SolrClient::threads

(PECL solr> = 0.9.2)

SolrClient::threads — Перевіряє статус тем

### Опис

```methodsynopsis
public SolrClient::threads(): void
```

Перевіряє статус тем

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт SolrGenericResponse.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.
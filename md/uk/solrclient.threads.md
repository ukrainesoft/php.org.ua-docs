Перевіряє статус тем

-   [« SolrClient::system](solrclient.system.html)
    
-   [SolrResponse »](class.solrresponse.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
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

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.
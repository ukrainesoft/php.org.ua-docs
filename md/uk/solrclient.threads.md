---
navigation:
  - solrclient.system.md: '« SolrClient::system'
  - class.solrresponse.md: SolrResponse »
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::threads'
---
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

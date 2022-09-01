---
navigation:
  - solrclient.request.html: '« SolrClient::request'
  - solrclient.setresponsewriter.html: 'SolrClient::setResponseWriter »'
  - index.html: PHP Manual
  - class.solrclient.html: SolrClient
title: 'SolrClient::rollback'
---
# SolrClient::rollback

(PECL solr> = 0.9.2)

SolrClient::rollback - Відкочує всі додавання/видалення, зроблені в індекс з моменту останньої фіксації

### Опис

```methodsynopsis
public SolrClient::rollback(): SolrUpdateResponse
```

Відкочує всі додавання/видалення, зроблені індексом з моменту останньої фіксації. Він не викликає жодних прослуховувачів подій і не створює нового пошукача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає SolrUpdateResponse у разі успішного виконання або викидає виняток SolrClientException у разі виникнення помилки.

### Дивіться також

-   [SolrClient::commit()](solrclient.commit.md) - Завершує всі додавання/видалення, зроблені в індексі
-   [SolrClient::optimize()](solrclient.optimize.md) - дефрагментує індекс

---
navigation:
  - solrclient.request.md: '« SolrClient::request'
  - solrclient.setresponsewriter.md: 'SolrClient::setResponseWriter »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::rollback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::rollback

(PECL solr >= 0.9.2)

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

-   [SolrClient::commit()](solrclient.commit.md) \- Завершує всі додавання/видалення, зроблені в індексі
-   [SolrClient::optimize()](solrclient.optimize.md) \- дефрагментує індекс

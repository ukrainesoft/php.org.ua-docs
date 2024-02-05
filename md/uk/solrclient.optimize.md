---
navigation:
  - solrclient.getoptions.md: '« SolrClient::getOptions'
  - solrclient.ping.md: 'SolrClient::ping »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::optimize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::optimize

(PECL solr >= 0.9.2)

SolrClient::optimize - Дефрагментує індекс

### Опис

```methodsynopsis
public SolrClient::optimize(int $maxSegments = 1, bool $softCommit = true, bool $waitSearcher = true): SolrUpdateResponse
```

Дефрагментує індекс для прискорення пошуку.

### Список параметрів

`maxSegments`

Оптимізується до максимальної кількості сегментів. Починаючи із Solr 1.3

`softCommit`

Оновлює 'view' індексу продуктивніше, але без гарантій 'on-disk'. (Solr4.0+)

`waitSearcher`

Блокувати доти, доки не відкриється нова пошукова система і не буде зареєстрована як основна пошукова система, зробивши зміни видимими.

### Значення, що повертаються

Повертає SolrUpdateResponse у разі успішного виконання або викидає виняток у разі виникнення помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Примітки

**Увага**

PECL Solr >= 2.0 підтримує лише Solr Server >= 4.0

До PECL Solr 2.0 метод використовувався прийому аргументів "int $maxSegments, bool $waitFlush, bool $waitSearcher".

### Дивіться також

-   [SolrClient::commit()](solrclient.commit.md) \- Завершує всі додавання/видалення, зроблені в індексі
-   [SolrClient::rollback()](solrclient.rollback.md) \- Відкочує всі додавання/видалення, зроблені в індекс з моменту останньої фіксації

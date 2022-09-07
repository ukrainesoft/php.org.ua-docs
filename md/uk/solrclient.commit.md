---
navigation:
  - solrclient.adddocuments.md: '« SolrClient::addDocuments'
  - solrclient.construct.md: 'SolrClient::construct »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::commit'
---
# SolrClient::commit

(PECL solr> = 0.9.2)

SolrClient::commit — Завершує всі додавання/видалення, зроблені в індексі

### Опис

```methodsynopsis
public SolrClient::commit(bool $softCommit = false, bool $waitSearcher = true, bool $expungeDeletes = false): SolrUpdateResponse
```

Метод завершує всі додавання/видалення, зроблені в індексі.

### Список параметрів

`softCommit`

Оновлює 'view' індексу продуктивніше, але без гарантій 'on-disk'. (Solr4.0+)

М'яка фіксація виконується набагато швидше, оскільки вона робить видимими лише зміни індексу, а не файли індексу fsync та не записує новий дескриптор індексу. У разі збою JVM або втрати живлення зміни, що відбулися після останньої жорсткої фіксації, будуть втрачені. Колекції пошуку, які мають вимоги до роботи в режимі, близькому до реального часу (які хочуть, щоб зміни індексу були швидко видно для пошуку), захочуть частіше виконувати м'яку фіксацію, а жорстку фіксацію рідше.

`waitSearcher`

Блокувати доти, доки не відкриється нова пошукова система і не буде зареєстрована як основна пошукова система, зробивши зміни видимими.

`expungeDeletes`

Поєднати сегменти з видаленнями. (Solr1.4+)

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.md) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### список змін

| Версия | Описание |
| --- | --- |
| PECL solr 1.1.0, 2.0.0 | Видалено $maxSegments |
| PECL solr 2.0.0b | Зміни API: SolrClient::commit ( int $maxSegments = 0 , bool $softCommit = false , bool $waitSearcher = true, bool $expungeDeletes = false |
| PECL solr 0.9.2 | Сигнатура: SolrClient::commit ( int $maxSegments = 1 , bool $waitFlush = true , bool $waitSearcher = true ). $waitFlush: Блокувати, доки зміни індексу не будуть скинуті на диск. |

### Примітки

**Увага**

PECL Solr >= 2.0 підтримує лише Solr Server >= 4.0

### Дивіться також

-   [SolrClient::optimize()](solrclient.optimize.md) - дефрагментує індекс
-   [SolrClient::rollback()](solrclient.rollback.md) - Відкочує всі додавання/видалення, зроблені в індекс з моменту останньої фіксації

---
navigation:
  - solrobject.offsetunset.html: '« SolrObject::offsetUnset'
  - solrclient.adddocument.html: 'SolrClient::addDocument »'
  - index.html: PHP Manual
  - book.solr.html: Solr
title: Клас SolrClient
---
# Клас SolrClient

(PECL solr> = 0.9.2)

## Вступ

Використовується для надсилання запитів на сервер Solr. В даний час клонування та серіалізація екземплярів SolrClient не підтримується.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrClient
     
     {

    /* Константы */
    
     const
     int
      SEARCH_SERVLET_TYPE = 1;

    const
     int
      UPDATE_SERVLET_TYPE = 2;

    const
     int
      THREADS_SERVLET_TYPE = 4;

    const
     int
      PING_SERVLET_TYPE = 8;

    const
     int
      TERMS_SERVLET_TYPE = 16;

    const
     int
      SYSTEM_SERVLET_TYPE = 32;

    const
     string
      DEFAULT_SEARCH_SERVLET = select;

    const
     string
      DEFAULT_UPDATE_SERVLET = update;

    const
     string
      DEFAULT_THREADS_SERVLET = admin/threads;

    const
     string
      DEFAULT_PING_SERVLET = admin/ping;

    const
     string
      DEFAULT_TERMS_SERVLET = terms;

    const
     string
      DEFAULT_SYSTEM_SERVLET = admin/system;


    /* Методы */
    
   public __construct(array $clientOptions)

    public addDocument(SolrInputDocument $doc, bool $overwrite = true, int $commitWithin = 0): SolrUpdateResponse
public addDocuments(array $docs, bool $overwrite = true, int $commitWithin = 0): void
public commit(bool $softCommit = false, bool $waitSearcher = true, bool $expungeDeletes = false): SolrUpdateResponse
public deleteById(string $id): SolrUpdateResponse
public deleteByIds(array $ids): SolrUpdateResponse
public deleteByQueries(array $queries): SolrUpdateResponse
public deleteByQuery(string $query): SolrUpdateResponse
public getById(string $id): SolrQueryResponse
public getByIds(array $ids): SolrQueryResponse
public getDebug(): string
public getOptions(): array
public optimize(int $maxSegments = 1, bool $softCommit = true, bool $waitSearcher = true): SolrUpdateResponse
public ping(): SolrPingResponse
public query(SolrParams $query): SolrQueryResponse
public request(string $raw_request): SolrUpdateResponse
public rollback(): SolrUpdateResponse
public setResponseWriter(string $responseWriter): void
public setServlet(int $type, string $value): bool
public system(): void
public threads(): void

    public __destruct()

   }
```

## Обумовлені константи

**`SolrClient::SEARCH_SERVLET_TYPE`**

Використовується для оновлення сервлета пошуку.

**`SolrClient::UPDATE_SERVLET_TYPE`**

Використовується для оновлення сервлета оновлення.

**`SolrClient::THREADS_SERVLET_TYPE`**

Використовується для оновлення сервлета потоків.

**`SolrClient::PING_SERVLET_TYPE`**

Використовується для оновлення сервлета ping.

**`SolrClient::TERMS_SERVLET_TYPE`**

Використовується для оновлення термінів сервлет.

**`SolrClient::SYSTEM_SERVLET_TYPE`**

Використовується для отримання системної інформації із системного сервлета.

**`SolrClient::DEFAULT_SEARCH_SERVLET`**

Це початкове значення пошукового сервлета.

**`SolrClient::DEFAULT_UPDATE_SERVLET`**

Це початкове значення для сервлета оновлення.

**`SolrClient::DEFAULT_THREADS_SERVLET`**

Це початкове значення сервлета потоків.

**`SolrClient::DEFAULT_PING_SERVLET`**

Це початкове значення для ping сервлета.

**`SolrClient::DEFAULT_TERMS_SERVLET`**

Це початкове значення для термінів сервлет, що використовуються для TermsComponent

**`SolrClient::DEFAULT_SYSTEM_SERVLET`**

Це початкове значення для системного сервлета, який використовується для отримання інформації про сервер Solr.

## Зміст

-   [SolrClient::addDocument](solrclient.adddocument.html) — Додає документ до індексу
-   [SolrClient::addDocuments](solrclient.adddocuments.html) — Додає колекцію екземплярів SolrInputDocument до індексу
-   [SolrClient::commit](solrclient.commit.html) — Завершує всі додавання/видалення, зроблені в індексі
-   [SolrClient::construct](solrclient.construct.html) - Конструктор об'єкта SolrClient
-   [SolrClient::deleteById](solrclient.deletebyid.html) — Видаляє за ідентифікатором
-   [SolrClient::deleteByIds](solrclient.deletebyids.html) — Видаляє за ідентифікаторами
-   [SolrClient::deleteByQueries](solrclient.deletebyqueries.html) — Видаляє всі документи, що відповідають будь-якому запиту.
-   [SolrClient::deleteByQuery](solrclient.deletebyquery.html) — Видаляє всі документи, які відповідають заданому запиту
-   [SolrClient::destruct](solrclient.destruct.html) - Деструктор SolrClient
-   [SolrClient::getById](solrclient.getbyid.html) — Отримує документ щодо ідентифікатора. Використовує Solr Realtime Get (RTG)
-   [SolrClient::getByIds](solrclient.getbyids.html) — Отримує документи щодо їх ідентифікаторів. Використовує Solr Realtime Get (RTG)
-   [SolrClient::getDebug](solrclient.getdebug.html) — Повертає дані налагодження для останньої спроби підключення
-   [SolrClient::getOptions](solrclient.getoptions.html) - Повертає внутрішні параметри клієнта
-   [SolrClient::optimize](solrclient.optimize.html) - Дефрагментує індекс
-   [SolrClient::ping](solrclient.ping.html) — Перевіряє, чи сервер Solr працює
-   [SolrClient::query](solrclient.query.html) — Надсилає запит на сервер
-   [SolrClient::request](solrclient.request.html) — Надсилає необроблений запит на оновлення
-   [SolrClient::rollback](solrclient.rollback.html) — Відкочує всі додавання/видалення, зроблені в індекс з моменту останньої фіксації
-   [SolrClient::setResponseWriter](solrclient.setresponsewriter.html) - Встановлює письменник відповіді, що використовується для підготовки відповіді від Solr
-   [SolrClient::setServlet](solrclient.setservlet.html) — Змінює вказаний тип сервлету на нове значення
-   [SolrClient::system](solrclient.system.html) — Отримує інформацію про сервер Solr
-   [SolrClient::threads](solrclient.threads.html) — Перевіряє статус тем

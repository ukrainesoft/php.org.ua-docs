---
navigation:
  - class.solrutils.md: « SolrUtils
  - solrutils.escapequerychars.md: 'SolrUtils::escapeQueryChars »'
  - index.md: PHP Manual
  - class.solrutils.md: SolrUtils
title: 'SolrUtils::digestXmlResponse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrUtils::digestXmlResponse

(PECL solr >= 0.9.2)

SolrUtils::digestXmlResponse — Перетворює XML-рядок відповіді на об'єкт SolrObject

### Опис

```methodsynopsis
public static SolrUtils::digestXmlResponse(string $xmlresponse, int $parse_mode = 0): SolrObject
```

Метод перетворює XML-рядок відповіді з сервера Apache Solr на об'єкт SolrObject. У разі помилки викидає виняток SolrException.

### Список параметрів

`xmlresponse`

Рядок відповіді XML від сервера Solr.

`parse_mode`

Доступні значення: SolrResponse::PARSE\_SOLR\_OBJ або SolrResponse::PARSE\_SOLR\_DOC.

### Значення, що повертаються

Повертає об'єкт SolrObject, який представляє відповідь XML.

Якщо для параметра parse\_mode встановлено значення SolrResponse::PARSE\_SOLR\_OBJ, документи Solr будуть аналізуватись як екземпляри SolrObject.

Якщо встановлено значення SolrResponse::PARSE\_SOLR\_DOC, вони будуть проаналізовані як екземпляри SolrDocument.

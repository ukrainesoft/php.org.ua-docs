---
navigation:
  - solrdocument.valid.md: '« SolrDocument::valid'
  - solrdocumentfield.construct.md: 'SolrDocumentField::\_\_construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrDocumentField
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrDocumentField

(PECL solr >= 0.9.2)

## Вступ

Представляє поле у ​​документі Solr. Усі його властивості доступні лише читання.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrDocumentField
     
     {

    /* Свойства */
    
     public
     readonly
     string
      $name;

    public
     readonly
     float
      $boost;

    public
     readonly
     array
      $values;



    /* Методы */
    
   public __construct()

    public __destruct()

   }
```

## Властивості

name

Назва поля.

boost

Значення підвищення поля

values

Масив значень для цього поля

## Зміст

-   [SolrDocumentField::\_\_construct](solrdocumentfield.construct.md) \- Конструктор
-   [SolrDocumentField::\_\_destruct](solrdocumentfield.destruct.md) \- Деструктор

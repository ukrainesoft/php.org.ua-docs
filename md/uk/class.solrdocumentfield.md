---
navigation:
  - solrdocument.valid.md: '« SolrDocument::valid'
  - solrdocumentfield.construct.md: 'SolrDocumentField::construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrDocumentField
---
# Клас SolrDocumentField

(PECL solr> = 0.9.2)

## Вступ

Представляє поле у ​​документі Solr. Усі його властивості доступні лише читання.

## Огляд класів

```synopsis



    
     
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

-   [SolrDocumentField::construct](solrdocumentfield.construct.md) - Конструктор
-   [SolrDocumentField::destruct](solrdocumentfield.destruct.md) - Деструктор

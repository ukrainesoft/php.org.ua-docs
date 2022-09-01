---
navigation:
  - solrdocumentfield.destruct.html: '« SolrDocumentField::destruct'
  - solrobject.construct.html: 'SolrObject::construct »'
  - index.html: PHP Manual
  - book.solr.html: Solr
title: Клас SolrObject
---
# Клас SolrObject

(PECL solr> = 0.9.2)

## Вступ

Об'єкт, властивості якого можна отримати за допомогою синтаксису масиву. Усі його властивості доступні лише читання.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrObject
     

     implements 
       ArrayAccess {


    /* Методы */
    
   public __construct()

    public getPropertyNames(): array
public offsetExists(string $property_name): bool
public offsetGet(string $property_name): mixed
public offsetSet(string $property_name, string $property_value): void
public offsetUnset(string $property_name): void

    public __destruct()

   }
```

## Зміст

-   [SolrObject::construct](solrobject.construct.html) — Створює об'єкт Solr
-   [SolrObject::destruct](solrobject.destruct.html) - Деструктор
-   [SolrObject::getPropertyNames](solrobject.getpropertynames.html) - Повертає масив усіх імен властивостей
-   [SolrObject::offsetExists](solrobject.offsetexists.html) — Перевіряє, чи існує властивість
-   [SolrObject::offsetGet](solrobject.offsetget.html) — Використовується для отримання якості
-   [SolrObject::offsetSet](solrobject.offsetset.html) - Встановлює значення властивості
-   [SolrObject::offsetUnset](solrobject.offsetunset.html) - Скидає значення властивості

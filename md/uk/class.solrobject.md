---
navigation:
  - solrdocumentfield.destruct.md: '« SolrDocumentField::destruct'
  - solrobject.construct.md: 'SolrObject::construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
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

-   [SolrObject::construct](solrobject.construct.md) — Створює об'єкт Solr
-   [SolrObject::destruct](solrobject.destruct.md) - Деструктор
-   [SolrObject::getPropertyNames](solrobject.getpropertynames.md) - Повертає масив усіх імен властивостей
-   [SolrObject::offsetExists](solrobject.offsetexists.md) — Перевіряє, чи існує властивість
-   [SolrObject::offsetGet](solrobject.offsetget.md) — Використовується для отримання якості
-   [SolrObject::offsetSet](solrobject.offsetset.md) - Встановлює значення властивості
-   [SolrObject::offsetUnset](solrobject.offsetunset.md) - Скидає значення властивості

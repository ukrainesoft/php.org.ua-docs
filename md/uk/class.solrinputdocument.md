Клас SolrInputDocument

-   [« SolrUtils::queryPhrase](solrutils.queryphrase.html)
    
-   [SolrInputDocument::addChildDocument »](solrinputdocument.addchilddocument.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrInputDocument
    

# Клас SolrInputDocument

(PECL solr> = 0.9.2)

## Вступ

Цей клас представляє документ Solr, який буде відправлено до індексу Solr.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrInputDocument
     
     {

    /* Константы */
    
     const
     int
      SORT_DEFAULT = 1;

    const
     int
      SORT_ASC = 1;

    const
     int
      SORT_DESC = 2;

    const
     int
      SORT_FIELD_NAME = 1;

    const
     int
      SORT_FIELD_VALUE_COUNT = 2;

    const
     int
      SORT_FIELD_BOOST_VALUE = 4;


    /* Методы */
    
   public __construct()

    public addChildDocument(SolrInputDocument $child): void
public addChildDocuments(array &$docs): void
public addField(string $fieldName, string $fieldValue, float $fieldBoostValue = 0.0): bool
public clear(): bool
public __clone(): void
public deleteField(string $fieldName): bool
public fieldExists(string $fieldName): bool
public getBoost(): float
public getChildDocuments(): array
public getChildDocumentsCount(): int
public getField(string $fieldName): SolrDocumentField
public getFieldBoost(string $fieldName): float
public getFieldCount(): int|false
public getFieldNames(): array
public hasChildDocuments(): bool
public merge(SolrInputDocument $sourceDoc, bool $overwrite = true): bool
public reset(): bool
public setBoost(float $documentBoostValue): bool
public setFieldBoost(string $fieldName, float $fieldBoostValue): bool
public sort(int $sortOrderBy, int $sortDirection = SolrInputDocument::SORT_ASC): bool
public toArray(): array

    public __destruct()

   }
```

## Обумовлені константи

## Константи класу SolrInputDocument

**`SolrInputDocument::SORT_DEFAULT`**

Сортує поля у порядку зростання.

**`SolrInputDocument::SORT_ASC`**

Сортує поля у порядку зростання.

**`SolrInputDocument::SORT_DESC`**

Сортує поля у порядку спадання.

**`SolrInputDocument::SORT_FIELD_NAME`**

Сортує поля на ім'я

**`SolrInputDocument::SORT_FIELD_VALUE_COUNT`**

Сортує поля за кількістю значень.

**`SolrInputDocument::SORT_FIELD_BOOST_VALUE`**

Сортує поля за значенням підвищення.

## Зміст

-   [SolrInputDocument::addChildDocument](solrinputdocument.addchilddocument.html) — Додає дочірній документ для блокової індексації
-   [SolrInputDocument::addChildDocuments](solrinputdocument.addchilddocuments.html) — Додає масив дочірніх документів
-   [SolrInputDocument::addField](solrinputdocument.addfield.html) — Додає поле до документа
-   [SolrInputDocument::clear](solrinputdocument.clear.html) — скидає вхідний документ
-   [SolrInputDocument::\_\_clone](solrinputdocument.clone.html) - Створює копію SolrDocument
-   [SolrInputDocument::\_\_construct](solrinputdocument.construct.html) - Конструктор
-   [SolrInputDocument::deleteField](solrinputdocument.deletefield.html) — Видаляє поле із документа
-   [SolrInputDocument::\_\_destruct](solrinputdocument.destruct.html) - Деструктор
-   [SolrInputDocument::fieldExists](solrinputdocument.fieldexists.html) — Перевіряє, чи є поле
-   [SolrInputDocument::getBoost](solrinputdocument.getboost.html) — Отримує поточне значення підвищення документа
-   [SolrInputDocument::getChildDocuments](solrinputdocument.getchilddocuments.html) - Повертає масив дочірніх документів (SolrInputDocument)
-   [SolrInputDocument::getChildDocumentsCount](solrinputdocument.getchilddocumentscount.html) — Повертає кількість дочірніх документів
-   [SolrInputDocument::getField](solrinputdocument.getfield.html) — Отримує поле на ім'я
-   [SolrInputDocument::getFieldBoost](solrinputdocument.getfieldboost.html) — Отримує значення підвищення для певного поля
-   [SolrInputDocument::getFieldCount](solrinputdocument.getfieldcount.html) — Повертає кількість полів у документі
-   [SolrInputDocument::getFieldNames](solrinputdocument.getfieldnames.html) — Повертає масив, що містить усі поля у документі
-   [SolrInputDocument::hasChildDocuments](solrinputdocument.haschilddocuments.html) — Повертає true, якщо документ має дочірні документи.
-   [SolrInputDocument::merge](solrinputdocument.merge.html) — Об'єднує один вхідний документ до іншого
-   [SolrInputDocument::reset](solrinputdocument.reset.html) - Псевдонім SolrInputDocument::clear
-   [SolrInputDocument::setBoost](solrinputdocument.setboost.html) — Встановлює значення підвищення документа
-   [SolrInputDocument::setFieldBoost](solrinputdocument.setfieldboost.html) — Встановлює значення підвищення індексу часу для поля
-   [SolrInputDocument::sort](solrinputdocument.sort.html) — Сортує поля у документі
-   [SolrInputDocument::toArray](solrinputdocument.toarray.html) — Повертає подання масиву вхідного документа
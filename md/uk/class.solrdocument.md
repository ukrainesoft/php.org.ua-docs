---
navigation:
  - solrinputdocument.toarray.md: '« SolrInputDocument::toArray'
  - solrdocument.addfield.md: 'SolrDocument::addField »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrDocument
---
# Клас SolrDocument

(PECL solr> = 0.9.2)

## Вступ

Подає документ Solr, отриманий з відповіді запит.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrDocument
     

     implements 
       ArrayAccess,  Iterator,  Serializable {

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

    public addField(string $fieldName, string $fieldValue): bool
public clear(): bool
public __clone(): void
public current(): SolrDocumentField
public deleteField(string $fieldName): bool
public fieldExists(string $fieldName): bool
public __get(string $fieldName): SolrDocumentField
public getChildDocuments(): array
public getChildDocumentsCount(): int
public getField(string $fieldName): SolrDocumentField
public getFieldCount(): int
public getFieldNames(): array
public getInputDocument(): SolrInputDocument
public hasChildDocuments(): bool
public __isset(string $fieldName): bool
public key(): string
public merge(SolrDocument $sourceDoc, bool $overwrite = true): bool
public next(): void
public offsetExists(string $fieldName): bool
public offsetGet(string $fieldName): SolrDocumentField
public offsetSet(string $fieldName, string $fieldValue): void
public offsetUnset(string $fieldName): void
public reset(): bool
public rewind(): void
public serialize(): string
public __set(string $fieldName, string $fieldValue): bool
public sort(int $sortOrderBy, int $sortDirection = SolrDocument::SORT_ASC): bool
public toArray(): array
public unserialize(string $serialized): void
public __unset(string $fieldName): bool
public valid(): bool

    public __destruct()

   }
```

## Обумовлені константи

**`SolrDocument::SORT_DEFAULT`**

Стандартний режим для сортування полів у документі.

**`SolrDocument::SORT_ASC`**

Сортує поля у порядку зростання

**`SolrDocument::SORT_DESC`**

Сортує поля в порядку зменшення

**`SolrDocument::SORT_FIELD_NAME`**

Сортує поля на ім'я поля.

**`SolrDocument::SORT_FIELD_VALUE_COUNT`**

Сортує поля за кількістю значень у кожному полі.

**`SolrDocument::SORT_FIELD_BOOST_VALUE`**

Сортує поля за значенням посилення.

## Зміст

-   [SolrDocument::addField](solrdocument.addfield.md) — Додає поле до документа
-   [SolrDocument::clear](solrdocument.clear.md) — Видаляє всі поля у документі
-   [SolrDocument::clone](solrdocument.clone.md) — Створює копію об'єкта SolrDocument
-   [SolrDocument::construct](solrdocument.construct.md) - Конструктор
-   [SolrDocument::current](solrdocument.current.md) — Отримує поточне поле
-   [SolrDocument::deleteField](solrdocument.deletefield.md) — Видаляє поле із документа
-   [SolrDocument::destruct](solrdocument.destruct.md) - Деструктор
-   [SolrDocument::fieldExists](solrdocument.fieldexists.md) — Перевіряє, чи є поле у ​​документі
-   [SolrDocument::get](solrdocument.get.md) — Доступ до поля як властивості
-   [SolrDocument::getChildDocuments](solrdocument.getchilddocuments.md) - Повертає масив дочірніх документів (SolrDocument)
-   [SolrDocument::getChildDocumentsCount](solrdocument.getchilddocumentscount.md) — Повертає кількість дочірніх документів
-   [SolrDocument::getField](solrdocument.getfield.md) — Отримує поле на ім'я
-   [SolrDocument::getFieldCount](solrdocument.getfieldcount.md) — Повертає кількість полів у цьому документі
-   [SolrDocument::getFieldNames](solrdocument.getfieldnames.md) — Повертає масив імен полів у документі
-   [SolrDocument::getInputDocument](solrdocument.getinputdocument.md) — Повертає SolrInputDocument еквівалент об'єкту
-   [SolrDocument::hasChildDocuments](solrdocument.haschilddocuments.md) — Перевіряє, чи документ має дочірні документи.
-   [SolrDocument::isset](solrdocument.isset.md) — Перевіряє, чи є поле
-   [SolrDocument::key](solrdocument.key.md) — Отримує поточний ключ
-   [SolrDocument::merge](solrdocument.merge.md) — Зливає джерело у поточний SolrDocument
-   [SolrDocument::next](solrdocument.next.md) — Переміщує внутрішній покажчик на наступне поле
-   [SolrDocument::offsetExists](solrdocument.offsetexists.md) — Перевіряє, чи існує конкретне поле
-   [SolrDocument::offsetGet](solrdocument.offsetget.md) — Отримує поле
-   [SolrDocument::offsetSet](solrdocument.offsetset.md) — Додає поле до документа
-   [SolrDocument::offsetUnset](solrdocument.offsetunset.md) - Видаляє поле
-   [SolrDocument::reset](solrdocument.reset.md) - Псевдонім SolrDocument::clear()
-   [SolrDocument::rewind](solrdocument.rewind.md) — скидає внутрішній покажчик на початок
-   [SolrDocument::serialize](solrdocument.serialize.md) — Використовується для серіалізації користувача
-   [SolrDocument::set](solrdocument.set.md) — Додає ще одне поле до документа
-   [SolrDocument::sort](solrdocument.sort.md) — Сортує поля у документі
-   [SolrDocument::toArray](solrdocument.toarray.md) — Повертає подання масиву документа
-   [SolrDocument::unserialize](solrdocument.unserialize.md) — Серіалізація об'єктів користувача SolrDocument
-   [SolrDocument::unset](solrdocument.unset.md) — Видаляє поле із документа
-   [SolrDocument::valid](solrdocument.valid.md) — Перевіряє, чи поточна позиція є внутрішньо коректною.

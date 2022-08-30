Клас SolrDocument

-   [« SolrInputDocument::toArray](solrinputdocument.toarray.html)
    
-   [SolrDocument::addField »](solrdocument.addfield.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrDocument
    

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

-   [SolrDocument::addField](solrdocument.addfield.html) — Додає поле до документа
-   [SolrDocument::clear](solrdocument.clear.html) — Видаляє всі поля у документі
-   [SolrDocument::clone](solrdocument.clone.html) — Створює копію об'єкта SolrDocument
-   [SolrDocument::construct](solrdocument.construct.html) - Конструктор
-   [SolrDocument::current](solrdocument.current.html) — Отримує поточне поле
-   [SolrDocument::deleteField](solrdocument.deletefield.html) — Видаляє поле із документа
-   [SolrDocument::destruct](solrdocument.destruct.html) - Деструктор
-   [SolrDocument::fieldExists](solrdocument.fieldexists.html) — Перевіряє, чи є поле у ​​документі
-   [SolrDocument::get](solrdocument.get.html) — Доступ до поля як властивості
-   [SolrDocument::getChildDocuments](solrdocument.getchilddocuments.html) - Повертає масив дочірніх документів (SolrDocument)
-   [SolrDocument::getChildDocumentsCount](solrdocument.getchilddocumentscount.html) — Повертає кількість дочірніх документів
-   [SolrDocument::getField](solrdocument.getfield.html) — Отримує поле на ім'я
-   [SolrDocument::getFieldCount](solrdocument.getfieldcount.html) — Повертає кількість полів у цьому документі
-   [SolrDocument::getFieldNames](solrdocument.getfieldnames.html) — Повертає масив імен полів у документі
-   [SolrDocument::getInputDocument](solrdocument.getinputdocument.html) — Повертає SolrInputDocument еквівалент об'єкту
-   [SolrDocument::hasChildDocuments](solrdocument.haschilddocuments.html) — Перевіряє, чи документ має дочірні документи.
-   [SolrDocument::isset](solrdocument.isset.html) — Перевіряє, чи є поле
-   [SolrDocument::key](solrdocument.key.html) — Отримує поточний ключ
-   [SolrDocument::merge](solrdocument.merge.html) — Зливає джерело у поточний SolrDocument
-   [SolrDocument::next](solrdocument.next.html) — Переміщує внутрішній покажчик на наступне поле
-   [SolrDocument::offsetExists](solrdocument.offsetexists.html) — Перевіряє, чи існує конкретне поле
-   [SolrDocument::offsetGet](solrdocument.offsetget.html) — Отримує поле
-   [SolrDocument::offsetSet](solrdocument.offsetset.html) — Додає поле до документа
-   [SolrDocument::offsetUnset](solrdocument.offsetunset.html) - Видаляє поле
-   [SolrDocument::reset](solrdocument.reset.html) - Псевдонім SolrDocument::clear()
-   [SolrDocument::rewind](solrdocument.rewind.html) — скидає внутрішній покажчик на початок
-   [SolrDocument::serialize](solrdocument.serialize.html) — Використовується для серіалізації користувача
-   [SolrDocument::set](solrdocument.set.html) — Додає ще одне поле до документа
-   [SolrDocument::sort](solrdocument.sort.html) — Сортує поля у документі
-   [SolrDocument::toArray](solrdocument.toarray.html) — Повертає подання масиву документа
-   [SolrDocument::unserialize](solrdocument.unserialize.html) — Серіалізація об'єктів користувача SolrDocument
-   [SolrDocument::unset](solrdocument.unset.html) — Видаляє поле із документа
-   [SolrDocument::valid](solrdocument.valid.html) — Перевіряє, чи поточна позиція є внутрішньо коректною.
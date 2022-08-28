Клас SolrCollapseFunction

-   [« SolrDisMaxQuery::useEDisMaxQueryParser](solrdismaxquery.useedismaxqueryparser.html)
    
-   [SolrCollapseFunction::\_\_construct »](solrcollapsefunction.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrCollapseFunction
    

# Клас SolrCollapseFunction

(PECL solr> = 2.2.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class SolrCollapseFunction
     
     {

    /* Константы */
    
     const
     string
      NULLPOLICY_IGNORE = ignore;

    const
     string
      NULLPOLICY_EXPAND = expand;

    const
     string
      NULLPOLICY_COLLAPSE = collapse;


    /* Методы */
    
   public __construct(string $field = ?)

    public getField(): string
public getHint(): string
public getMax(): string
public getMin(): string
public getNullPolicy(): string
public getSize(): int
public setField(string $fieldName): SolrCollapseFunction
public setHint(string $hint): SolrCollapseFunction
public setMax(string $max): SolrCollapseFunction
public setMin(string $min): SolrCollapseFunction
public setNullPolicy(string $nullPolicy): SolrCollapseFunction
public setSize(int $size): SolrCollapseFunction
public __toString(): string

   }
```

## Обумовлені константи

**`SolrCollapseFunction::NULLPOLICY_IGNORE`**

**`SolrCollapseFunction::NULLPOLICY_EXPAND`**

**`SolrCollapseFunction::NULLPOLICY_COLLAPSE`**

## Зміст

-   [SolrCollapseFunction::\_\_construct](solrcollapsefunction.construct.html) - Конструктор класу
-   [SolrCollapseFunction::getField](solrcollapsefunction.getfield.html) - Повертає згорнуте поле
-   [SolrCollapseFunction::getHint](solrcollapsefunction.gethint.html) — Повертає підказку згортання
-   [SolrCollapseFunction::getMax](solrcollapsefunction.getmax.html) — Повертає максимальне значення
-   [SolrCollapseFunction::getMin](solrcollapsefunction.getmin.html) — Повертає мінімальне значення
-   [SolrCollapseFunction::getNullPolicy](solrcollapsefunction.getnullpolicy.html) — Повертає політику NULL
-   [SolrCollapseFunction::getSize](solrcollapsefunction.getsize.html) — Повертає параметр розміру
-   [SolrCollapseFunction::setField](solrcollapsefunction.setfield.html) — Встановлює поле для згортання
-   [SolrCollapseFunction::setHint](solrcollapsefunction.sethint.html) - Встановлює підказку згортання
-   [SolrCollapseFunction::setMax](solrcollapsefunction.setmax.html) — Вибирає заголовки групи за максимальним значенням числового поля або запитом функції
-   [SolrCollapseFunction::setMin](solrcollapsefunction.setmin.html) — Встановлює початковий розмір структур даних, що згортаються, тільки при згортанні за числовим полем
-   [SolrCollapseFunction::setNullPolicy](solrcollapsefunction.setnullpolicy.html) - Встановлює NULL-політику
-   [SolrCollapseFunction::setSize](solrcollapsefunction.setsize.html) — Встановлює початковий розмір структур даних, що згортаються, тільки при згортанні за числовим полем
-   [SolrCollapseFunction::\_\_toString](solrcollapsefunction.tostring.html) — Повертає рядок, який представляє побудовану функцію згортання
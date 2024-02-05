---
navigation:
  - solrdismaxquery.useedismaxqueryparser.md: '« SolrDisMaxQuery::useEDisMaxQueryParser'
  - solrcollapsefunction.construct.md: 'SolrCollapseFunction::\_\_construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrCollapseFunction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrCollapseFunction

(PECL solr >= 2.2.0)

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

-   [SolrCollapseFunction::\_\_construct](solrcollapsefunction.construct.md) \- Конструктор класу
-   [SolrCollapseFunction::getField](solrcollapsefunction.getfield.md) \- Повертає згорнуте поле
-   [SolrCollapseFunction::getHint](solrcollapsefunction.gethint.md)— Повертає підказку згортання
-   [SolrCollapseFunction::getMax](solrcollapsefunction.getmax.md)— Повертає максимальне значення
-   [SolrCollapseFunction::getMin](solrcollapsefunction.getmin.md)— Повертає мінімальне значення
-   [SolrCollapseFunction::getNullPolicy](solrcollapsefunction.getnullpolicy.md)— Повертає політику NULL
-   [SolrCollapseFunction::getSize](solrcollapsefunction.getsize.md)— Повертає параметр розміру
-   [SolrCollapseFunction::setField](solrcollapsefunction.setfield.md)— Встановлює поле для згортання
-   [SolrCollapseFunction::setHint](solrcollapsefunction.sethint.md) \- Встановлює підказку згортання
-   [SolrCollapseFunction::setMax](solrcollapsefunction.setmax.md)— Вибирає заголовки групи за максимальним значенням числового поля або запитом функції
-   [SolrCollapseFunction::setMin](solrcollapsefunction.setmin.md)— Встановлює початковий розмір структур даних, що згортаються, тільки при згортанні за числовим полем
-   [SolrCollapseFunction::setNullPolicy](solrcollapsefunction.setnullpolicy.md) \- Встановлює NULL-політику
-   [SolrCollapseFunction::setSize](solrcollapsefunction.setsize.md)— Встановлює початковий розмір структур даних, що згортаються, тільки при згортанні за числовим полем
-   [SolrCollapseFunction::\_\_function toString() { \[native code\] }](solrcollapsefunction.tostring.md)— Повертає рядок, який представляє побудовану функцію згортання

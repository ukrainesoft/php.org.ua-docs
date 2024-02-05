---
navigation:
  - domtext.splittext.md: '« DOMText::splitText'
  - domxpath.construct.md: 'DOMXPath::\_\_construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMXPath
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMXPath

(PHP 5, PHP 7, PHP 8)

## Вступ

Підтримує XPath 1.0

## Огляд класів

```classsynopsis

    
     class DOMXPath
     {

    /* Свойства */
    
     public
     readonly
     DOMDocument
      $document;


    public
     bool
      $registerNodeNamespaces;


    /* Методы */
    
   public __construct(DOMDocument $document, bool $registerNodeNS = true)

    public evaluate(string $expression, ?DOMNode $contextNode = null, bool $registerNodeNS = true): mixed
public query(string $expression, ?DOMNode $contextNode = null, bool $registerNodeNS = true): mixed
public registerNamespace(string $prefix, string $namespace): bool
public registerPhpFunctions(string|array|null $restrict = null): void

   }
```

## Властивості

document

registerNodeNamespaces

Если установлено значение\*\*`true`\*\*, простір імен реєструються у вузлі.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Додано властивість registerNodeNamespaces. |

## Зміст

-   [DOMXPath::\_\_construct](domxpath.construct.md)— Створює новий об'єкт класу DOMXPath
-   [DOMXPath::evaluate](domxpath.evaluate.md)— Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо
-   [DOMXPath::query](domxpath.query.md)— Виконує заданий вираз XPath
-   [DOMXPath::registerNamespace](domxpath.registernamespace.md)— Реєструє простір імен з об'єктом DOMXPath
-   [DOMXPath::registerPhpFunctions](domxpath.registerphpfunctions.md) \- Реєстрація PHP-функцій як функцій XPath

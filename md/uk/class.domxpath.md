Клас DOMXPath

-   [« DOMText::splitText](domtext.splittext.html)
    
-   [DOMXPath::\_\_construct »](domxpath.construct.html)
    
-   [PHP Manual](index.html)
    
-   [DOM](book.dom.html)
    
-   Клас DOMXPath
    

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

Якщо встановлено значення **`true`**, простір імен реєструються у вузлі.

## список змін

| Версия | Описание                                   |
|--------|--------------------------------------------|
|        | Додано властивість registerNodeNamespaces. |

## Зміст

-   [DOMXPath::\_\_construct](domxpath.construct.html) — Створює новий об'єкт класу DOMXPath
-   [DOMXPath::evaluate](domxpath.evaluate.html) — Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо
-   [DOMXPath::query](domxpath.query.html) — Виконує заданий вираз XPath
-   [DOMXPath::registerNamespace](domxpath.registernamespace.html) — Реєструє простір імен з об'єктом DOMXPath
-   [DOMXPath::registerPhpFunctions](domxpath.registerphpfunctions.html) - Реєстрація PHP-функцій як функцій XPath
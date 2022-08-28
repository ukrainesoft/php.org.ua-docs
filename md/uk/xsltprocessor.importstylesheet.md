Імпортує таблицю стилів

-   [« XSLTProcessor::hasExsltSupport](xsltprocessor.hasexsltsupport.html)
    
-   [XSLTProcessor::registerPHPFunctions »](xsltprocessor.registerphpfunctions.html)
    
-   [PHP Manual](index.html)
    
-   [XSLTProcessor](class.xsltprocessor.html)
    
-   Імпортує таблицю стилів
    

# XSLTProcessor::importStylesheet

(PHP 5, PHP 7, PHP 8)

XSLTProcessor::importStylesheet — Імпортує таблицю стилів

### Опис

```methodsynopsis
public
   XSLTProcessor::importStylesheet(object $stylesheet): bool
```

Цей метод імпортує таблицю стилів у [XSLTProcessor](class.xsltprocessor.html) для трансформації.

### Список параметрів

`stylesheet`

Імпортована таблиця стилів у вигляді об'єкта [DOMDocument](class.domdocument.html) або [SimpleXMLElement](class.simplexmlelement.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
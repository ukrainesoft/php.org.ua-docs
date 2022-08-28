Клас XSLTProcessor

-   [« Обработка ошибок с помощью функций обработки ошибок libxml](xsl.examples-errors.html)
    
-   [XSLTProcessor::\_\_construct »](xsltprocessor.construct.html)
    
-   [PHP Manual](index.html)
    
-   [XSL](book.xsl.html)
    
-   Клас XSLTProcessor
    

# Клас XSLTProcessor

(PHP 5, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class XSLTProcessor
     
     {

    /* Методы */
    
   public getParameter(string $namespace, string $name): string|false
public getSecurityPrefs(): int
public hasExsltSupport(): bool
public
   importStylesheet(object $stylesheet): bool
public registerPHPFunctions(array|string|null $functions = null): void
public removeParameter(string $namespace, string $name): bool
public setParameter(string $namespace, string $name, string $value): bool
public setParameter(string $namespace, array $options): bool
public setProfiling(?string $filename): bool
public setSecurityPrefs(int $preferences): int
public transformToDoc(object $document, ?string $returnClass = null): DOMDocument|false
public transformToURI(DOMDocument $doc, string $uri): int
public transformToXml(object $document): string|null|false

   }
```

## Зміст

-   [XSLTProcessor::\_\_construct](xsltprocessor.construct.html) — Створює новий екземпляр класу XSLTProcessor
-   [XSLTProcessor::getParameter](xsltprocessor.getparameter.html) — Повертає значення параметра
-   [XSLTProcessor::getSecurityPrefs](xsltprocessor.getsecurityprefs.html) — Отримати налаштування безпеки
-   [XSLTProcessor::hasExsltSupport](xsltprocessor.hasexsltsupport.html) — Чи визначає PHP підтримку EXSLT
-   [XSLTProcessor::importStylesheet](xsltprocessor.importstylesheet.html) - Імпортує таблицю стилів
-   [XSLTProcessor::registerPHPFunctions](xsltprocessor.registerphpfunctions.html) — Включає можливість використовувати PHP функції як функції XSLT
-   [XSLTProcessor::removeParameter](xsltprocessor.removeparameter.html) — Видаляє параметр
-   [XSLTProcessor::setParameter](xsltprocessor.setparameter.html) — Встановлює значення параметра
-   [XSLTProcessor::setProfiling](xsltprocessor.setprofiling.html) — Встановлює файл для профілювання
-   [XSLTProcessor::setSecurityPrefs](xsltprocessor.setsecurityprefs.html) — Встановити налаштування безпеки
-   [XSLTProcessor::transformToDoc](xsltprocessor.transformtodoc.html) — Перетворює на DOMDocument
-   [XSLTProcessor::transformToUri](xsltprocessor.transformtouri.html) — Перетворює на URI
-   [XSLTProcessor::transformToXml](xsltprocessor.transformtoxml.html) — Перетворює на XML
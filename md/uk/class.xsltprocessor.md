---
navigation:
  - xsl.examples-errors.md: « Обработка ошибок с помощью функций обработки ошибок libxml
  - xsltprocessor.construct.md: 'XSLTProcessor::construct »'
  - index.md: PHP Manual
  - book.xsl.md: XSL
title: Клас XSLTProcessor
---
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

-   [XSLTProcessor::construct](xsltprocessor.construct.md) — Створює новий екземпляр класу XSLTProcessor
-   [XSLTProcessor::getParameter](xsltprocessor.getparameter.md) — Повертає значення параметра
-   [XSLTProcessor::getSecurityPrefs](xsltprocessor.getsecurityprefs.md) — Отримати налаштування безпеки
-   [XSLTProcessor::hasExsltSupport](xsltprocessor.hasexsltsupport.md) — Чи визначає PHP підтримку EXSLT
-   [XSLTProcessor::importStylesheet](xsltprocessor.importstylesheet.md) - Імпортує таблицю стилів
-   [XSLTProcessor::registerPHPFunctions](xsltprocessor.registerphpfunctions.md) — Включає можливість використовувати PHP функції як функції XSLT
-   [XSLTProcessor::removeParameter](xsltprocessor.removeparameter.md) — Видаляє параметр
-   [XSLTProcessor::setParameter](xsltprocessor.setparameter.md) — Встановлює значення параметра
-   [XSLTProcessor::setProfiling](xsltprocessor.setprofiling.md) — Встановлює файл для профілювання
-   [XSLTProcessor::setSecurityPrefs](xsltprocessor.setsecurityprefs.md) — Встановити налаштування безпеки
-   [XSLTProcessor::transformToDoc](xsltprocessor.transformtodoc.md) — Перетворює на DOMDocument
-   [XSLTProcessor::transformToUri](xsltprocessor.transformtouri.md) — Перетворює на URI
-   [XSLTProcessor::transformToXml](xsltprocessor.transformtoxml.md) — Перетворює на XML

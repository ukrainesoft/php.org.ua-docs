---
navigation:
  - wkhtmltox.configuration.md: « Налаштування під час виконання
  - wkhtmltox-pdf-converter.add.html: 'wkhtmltoxPDFConverter::add »'
  - index.md: PHP Manual
  - book.wkhtmltox.md: wkhtmltox
title: Клас wkhtmltoxPDFConverter
---
# Клас wkhtmltoxPDFConverter

(wkhtmltox >= 0.1.0)

## Вступ

Перетворює вхідні дані HTML або набір вхідних даних HTML у PDF

## Огляд класів

```classsynopsis



    
     
      class wkhtmltox\PDF\Converter
     
     {


    /* Constructor */
    
   public __construct(array $settings = ?)


    /* Методы */
    public add(wkhtmltox\PDF\Object $object): void
public convert(): ?string
public getVersion(): string

   }
```

## Зміст

-   [wkhtmltoxPDFConverter::add](wkhtmltox-pdf-converter.add.md) — Додавання об'єкта для перетворення
-   [wkhtmltoxPDFConverter::construct](wkhtmltox-pdf-converter.construct.md) — Створити новий PDF-конвертер
-   [wkhtmltoxPDFConverter::convert](wkhtmltox-pdf-converter.convert.md) — Виконати перетворення PDF
-   [wkhtmltoxPDFConverter::getVersion](wkhtmltox-pdf-converter.getversion.md) — Визначити версію конвертера

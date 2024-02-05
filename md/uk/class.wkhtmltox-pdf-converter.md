---
navigation:
  - wkhtmltox.configuration.md: « Налаштування під час виконання
  - wkhtmltox-pdf-converter.add.md: 'wkhtmltox\\PDF\\Converter::add »'
  - index.md: PHP Manual
  - book.wkhtmltox.md: wkhtmltox
title: Клас wkhtmltox\\PDF\\Converter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас wkhtmltox\\PDF\\Converter

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

-   [wkhtmltox\\PDF\\Converter::add](wkhtmltox-pdf-converter.add.md)— Додавання об'єкта для перетворення
-   [wkhtmltox\\PDF\\Converter::\_\_construct](wkhtmltox-pdf-converter.construct.md)— Створити новий PDF-конвертер
-   [wkhtmltox\\PDF\\Converter::convert](wkhtmltox-pdf-converter.convert.md)— Виконати перетворення PDF
-   [wkhtmltox\\PDF\\Converter::getVersion](wkhtmltox-pdf-converter.getversion.md)— Визначити версію конвертера

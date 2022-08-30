Клас wkhtmltoxPDFConverter

-   [« Настройка во время выполнения](wkhtmltox.configuration.html)
    
-   [wkhtmltoxPDFConverter::add »](wkhtmltox-pdf-converter.add.html)
    
-   [PHP Manual](index.html)
    
-   [wkhtmltox](book.wkhtmltox.html)
    
-   Клас wkhtmltoxPDFConverter
    

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

-   [wkhtmltoxPDFConverter::add](wkhtmltox-pdf-converter.add.html) — Додавання об'єкта для перетворення
-   [wkhtmltoxPDFConverter::construct](wkhtmltox-pdf-converter.construct.html) — Створити новий PDF-конвертер
-   [wkhtmltoxPDFConverter::convert](wkhtmltox-pdf-converter.convert.html) — Виконати перетворення PDF
-   [wkhtmltoxPDFConverter::getVersion](wkhtmltox-pdf-converter.getversion.html) — Визначити версію конвертера
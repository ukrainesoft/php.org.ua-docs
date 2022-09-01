---
navigation:
  - yaf-request-simple.isxmlhttprequest.html: '« YafRequestSimple::isXmlHttpRequest'
  - yaf-response-abstract.appendbody.html: 'YafResponseAbstract::appendBody »'
  - index.html: PHP Manual
  - book.yaf.html: Yaf
title: Клас YafResponseAbstract
---
# Клас YafResponseAbstract

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Response_Abstract
     
     {
    
    /* Константы */
    
     const
     string
      DEFAULT_BODY = "content";


    /* Свойства */
    protected
      $_header;

    protected
      $_body;

    protected
      $_sendheader;



    /* Методы */
    
   public __construct()

    public appendBody(string $content, string $key = ?): bool
public clearBody(string $key = ?): bool
public clearHeaders(): void
public getBody(string $key = ?): mixed
public getHeader(): void
public prependBody(string $content, string $key = ?): bool
public response(): void
protected setAllHeaders(): void
public setBody(string $content, string $key = ?): bool
public setHeader(string $name, string $value, bool $replace = ?): bool
public setRedirect(string $url): bool
private __toString(): string

    public __destruct()

   }
```

## Властивості

header

body

sendheader

## Зміст

-   [YafResponseAbstract::appendBody](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [YafResponseAbstract::clearBody](yaf-response-abstract.clearbody.html) — Скидає все тіло відповіді, що існує.
-   [YafResponseAbstract::clearHeaders](yaf-response-abstract.clearheaders.html) - Скидає всі встановлені заголовки
-   [YafResponseAbstract::construct](yaf-response-abstract.construct.html) - Конструктор класу YafResponseAbstract
-   [YafResponseAbstract::destruct](yaf-response-abstract.destruct.html) - Деструктор класу YafResponseAbstract
-   [YafResponseAbstract::getBody](yaf-response-abstract.getbody.html) — Отримує наявний вміст
-   [YafResponseAbstract::getHeader](yaf-response-abstract.getheader.html) - Призначення getHeader
-   [YafResponseAbstract::prependBody](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [YafResponseAbstract::response](yaf-response-abstract.response.html) - Відправляє відповідь
-   [YafResponseAbstract::setAllHeaders](yaf-response-abstract.setallheaders.html) — Призначення setAllHeaders
-   [YafResponseAbstract::setBody](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [YafResponseAbstract::setHeader](yaf-response-abstract.setheader.html) - Встановлює заголовок відповіді
-   [YafResponseAbstract::setRedirect](yaf-response-abstract.setredirect.html) - Призначення setRedirect
-   [YafResponseAbstract::toString](yaf-response-abstract.tostring.html) — Отримує все тіло у вигляді рядка

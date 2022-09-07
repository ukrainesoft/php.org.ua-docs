---
navigation:
  - yaf-request-simple.isxmlhttprequest.md: '« YafRequestSimple::isXmlHttpRequest'
  - yaf-response-abstract.appendbody.md: 'YafResponseAbstract::appendBody »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
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

-   [YafResponseAbstract::appendBody](yaf-response-abstract.appendbody.md) - Додає вміст до тіла відповіді
-   [YafResponseAbstract::clearBody](yaf-response-abstract.clearbody.md) — Скидає все тіло відповіді, що існує.
-   [YafResponseAbstract::clearHeaders](yaf-response-abstract.clearheaders.md) - Скидає всі встановлені заголовки
-   [YafResponseAbstract::construct](yaf-response-abstract.construct.md) - Конструктор класу YafResponseAbstract
-   [YafResponseAbstract::destruct](yaf-response-abstract.destruct.md) - Деструктор класу YafResponseAbstract
-   [YafResponseAbstract::getBody](yaf-response-abstract.getbody.md) — Отримує наявний вміст
-   [YafResponseAbstract::getHeader](yaf-response-abstract.getheader.md) - Призначення getHeader
-   [YafResponseAbstract::prependBody](yaf-response-abstract.prependbody.md) - Призначення prependBody
-   [YafResponseAbstract::response](yaf-response-abstract.response.md) - Відправляє відповідь
-   [YafResponseAbstract::setAllHeaders](yaf-response-abstract.setallheaders.md) — Призначення setAllHeaders
-   [YafResponseAbstract::setBody](yaf-response-abstract.setbody.md) - Встановлює вміст відповіді
-   [YafResponseAbstract::setHeader](yaf-response-abstract.setheader.md) - Встановлює заголовок відповіді
-   [YafResponseAbstract::setRedirect](yaf-response-abstract.setredirect.md) - Призначення setRedirect
-   [YafResponseAbstract::toString](yaf-response-abstract.tostring.md) — Отримує все тіло у вигляді рядка

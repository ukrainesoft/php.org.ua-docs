---
navigation:
  - yaf-request-simple.isxmlhttprequest.md: '« Yaf\_Request\_Simple::isXmlHttpRequest'
  - yaf-response-abstract.appendbody.md: 'Yaf\_Response\_Abstract::appendBody »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Response\_Abstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Response\_Abstract

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

\_header

\_body

\_sendheader

## Зміст

-   [Yaf\_Response\_Abstract::appendBody](yaf-response-abstract.appendbody.md) \- Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::clearBody](yaf-response-abstract.clearbody.md)— Скидає все тіло відповіді, що існує.
-   [Yaf\_Response\_Abstract::clearHeaders](yaf-response-abstract.clearheaders.md) \- Скидає всі встановлені заголовки
-   [Yaf\_Response\_Abstract::\_\_construct](yaf-response-abstract.construct.md) \- Конструктор класу Yaf\_Response\_Abstract
-   [Yaf\_Response\_Abstract::\_\_destruct](yaf-response-abstract.destruct.md) \- Деструктор класу Yaf\_Response\_Abstract
-   [Yaf\_Response\_Abstract::getBody](yaf-response-abstract.getbody.md)— Отримує наявний вміст
-   [Yaf\_Response\_Abstract::getHeader](yaf-response-abstract.getheader.md) \- Призначення getHeader
-   [Yaf\_Response\_Abstract::prependBody](yaf-response-abstract.prependbody.md) \- Призначення prependBody
-   [Yaf\_Response\_Abstract::response](yaf-response-abstract.response.md) \- Відправляє відповідь
-   [Yaf\_Response\_Abstract::setAllHeaders](yaf-response-abstract.setallheaders.md)— Призначення setAllHeaders
-   [Yaf\_Response\_Abstract::setBody](yaf-response-abstract.setbody.md) \- Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::setHeader](yaf-response-abstract.setheader.md) \- Встановлює заголовок відповіді
-   [Yaf\_Response\_Abstract::setRedirect](yaf-response-abstract.setredirect.md) \- Призначення setRedirect
-   [Yaf\_Response\_Abstract::\_\_function toString() { \[native code\] }](yaf-response-abstract.tostring.md)— Отримує все тіло у вигляді рядка

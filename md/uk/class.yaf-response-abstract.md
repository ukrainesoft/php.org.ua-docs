Клас YafResponseAbstract

-   [« Yaf\_Request\_Simple::isXmlHttpRequest](yaf-request-simple.isxmlhttprequest.html)
    
-   [Yaf\_Response\_Abstract::appendBody »](yaf-response-abstract.appendbody.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafResponseAbstract
    

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

-   [Yaf\_Response\_Abstract::appendBody](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::clearBody](yaf-response-abstract.clearbody.html) — Скидає все тіло відповіді, що існує.
-   [Yaf\_Response\_Abstract::clearHeaders](yaf-response-abstract.clearheaders.html) - Скидає всі встановлені заголовки
-   [Yaf\_Response\_Abstract::\_\_construct](yaf-response-abstract.construct.html) - Конструктор класу YafResponseAbstract
-   [Yaf\_Response\_Abstract::\_\_destruct](yaf-response-abstract.destruct.html) - Деструктор класу YafResponseAbstract
-   [Yaf\_Response\_Abstract::getBody](yaf-response-abstract.getbody.html) — Отримує наявний вміст
-   [Yaf\_Response\_Abstract::getHeader](yaf-response-abstract.getheader.html) - Призначення getHeader
-   [Yaf\_Response\_Abstract::prependBody](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [Yaf\_Response\_Abstract::response](yaf-response-abstract.response.html) - Відправляє відповідь
-   [Yaf\_Response\_Abstract::setAllHeaders](yaf-response-abstract.setallheaders.html) — Призначення setAllHeaders
-   [Yaf\_Response\_Abstract::setBody](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::setHeader](yaf-response-abstract.setheader.html) - Встановлює заголовок відповіді
-   [Yaf\_Response\_Abstract::setRedirect](yaf-response-abstract.setredirect.html) - Призначення setRedirect
-   [Yaf\_Response\_Abstract::\_\_toString](yaf-response-abstract.tostring.html) — Отримує все тіло у вигляді рядка
Клас YafRequestHttp

-   [« YafRequestAbstract::setRouted](yaf-request-abstract.setrouted.html)
    
-   [YafRequestHttp::construct »](yaf-request-http.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRequestHttp
    

# Клас YafRequestHttp

(Yaf >=1.0.0)

## Вступ

Будь-який запит від клієнта ініціалізується як **YafRequestHttp**. Ви можете отримати інформацію про запит, наприклад URI і параметри запиту, використовуючи методи цього класу.

> **Зауваження**
> 
> З метою безпеки $GET/$POST доступні тільки для читання в Yaf, що означає, що якщо ви встановите значення для цих глобальних змінних, ви не зможете отримати їх за допомогою [YafRequestHttp::getQuery()](yaf-request-http.getquery.html) або [YafRequestHttp::getPost()](yaf-request-http.getpost.html)
> 
> Якщо виникає потреба у використанні такого функціоналу при модульному тестуванні, Yaf може бути зібраний за допомогою --enable-yaf-debug, який дозволить Yaf прочитати значення, задане користувачем через скрипт.
> 
> У цьому випадку Yaf видасть попередження ESTRICT, щоб нагадати про це: Strict Standards: you are running yaf in debug mode

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Request_Http
     

     
      extends
       Yaf_Request_Abstract
     
     {
    
    /* Свойства */


    /* Методы */
    
   public __construct(string $request_uri = ?, string $base_uri = ?)

    public get(string $name, string $default = ?): mixed
public getCookie(string $name, string $default = ?): mixed
public getFiles(): void
public getPost(string $name, string $default = ?): mixed
public getQuery(string $name, string $default = ?): mixed
public getRaw(): mixed
public getRequest(): void
public isXmlHttpRequest(): bool


    /* Наследуемые методы */
    public Yaf_Request_Abstract::clearParams(): bool
public Yaf_Request_Abstract::getActionName(): void
public Yaf_Request_Abstract::getBaseUri(): void
public Yaf_Request_Abstract::getControllerName(): void
public Yaf_Request_Abstract::getEnv(string $name, string $default = ?): void
public Yaf_Request_Abstract::getException(): void
public Yaf_Request_Abstract::getLanguage(): void
public Yaf_Request_Abstract::getMethod(): string
public Yaf_Request_Abstract::getModuleName(): void
public Yaf_Request_Abstract::getParam(string $name, string $default = ?): mixed
public Yaf_Request_Abstract::getParams(): array
public Yaf_Request_Abstract::getRequestUri(): void
public Yaf_Request_Abstract::getServer(string $name, string $default = ?): void
public Yaf_Request_Abstract::isCli(): bool
public Yaf_Request_Abstract::isDispatched(): bool
public Yaf_Request_Abstract::isGet(): bool
public Yaf_Request_Abstract::isHead(): bool
public Yaf_Request_Abstract::isOptions(): bool
public Yaf_Request_Abstract::isPost(): bool
public Yaf_Request_Abstract::isPut(): bool
public Yaf_Request_Abstract::isRouted(): bool
public Yaf_Request_Abstract::isXmlHttpRequest(): bool
public Yaf_Request_Abstract::setActionName(string $action, bool $format_name = true): void
public Yaf_Request_Abstract::setBaseUri(string $uir): bool
public Yaf_Request_Abstract::setControllerName(string $controller, bool $format_name = true): void
public Yaf_Request_Abstract::setDispatched(): void
public Yaf_Request_Abstract::setModuleName(string $module, bool $format_name = true): void
public Yaf_Request_Abstract::setParam(string $name, string $value = ?): bool
public Yaf_Request_Abstract::setRequestUri(string $uir): void
public Yaf_Request_Abstract::setRouted(string $flag = ?): void


   }
```

## Властивості

module

controller

action

метод

params

language

exception

baseuri

uri

dispatched

routed

## Зміст

-   [YafRequestHttp::construct](yaf-request-http.construct.html) - Конструктор класу YafRequestHttp
-   [YafRequestHttp::get](yaf-request-http.get.html) — Отримує змінну від клієнта
-   [YafRequestHttp::getCookie](yaf-request-http.getcookie.html) — Отримує змінну Cookie
-   [YafRequestHttp::getFiles](yaf-request-http.getfiles.html) - Призначення getFiles
-   [YafRequestHttp::getPost](yaf-request-http.getpost.html) — Отримує змінну POST
-   [YafRequestHttp::getQuery](yaf-request-http.getquery.html) — Отримує параметр запиту
-   [YafRequestHttp::getRaw](yaf-request-http.getraw.html) — Отримує необроблене тіло запиту
-   [YafRequestHttp::getRequest](yaf-request-http.getrequest.html) - Призначення getRequest
-   [YafRequestHttp::isXmlHttpRequest](yaf-request-http.isxmlhttprequest.html) — Визначає, чи є запит Ajax-запитом
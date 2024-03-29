---
navigation:
  - yaf-request-abstract.setrouted.md: '« Yaf\_Request\_Abstract::setRouted'
  - yaf-request-http.construct.md: 'Yaf\_Request\_Http::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Request\_Http
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Request\_Http

(Yaf >=1.0.0)

## Вступ

Будь-який запит від клієнта ініціалізується як **Yaf\_Request\_Http**. Ви можете отримати інформацію про запит, наприклад URI і параметри запиту, використовуючи методи цього класу.

> **Зауваження** :
> 
> З метою безпеки $\_GET/$\_POST доступні тільки для читання в Yaf, що означає, що якщо ви встановите значення для цих глобальних змінних, ви не зможете отримати їх за допомогою [Yaf\_Request\_Http::getQuery()](yaf-request-http.getquery.md) або [Yaf\_Request\_Http::getPost()](yaf-request-http.getpost.md)
> 
> Якщо виникає потреба у використанні такого функціоналу при модульному тестуванні, Yaf може бути зібраний за допомогою --enable-yaf-debug, який дозволить Yaf прочитати значення, задане користувачем через скрипт.
> 
> У цьому випадку Yaf видасть попередження E\_STRICT, щоб нагадати про це: Strict Standards: you are running yaf in debug mode

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

method

params

language

\_exception

\_base\_uri

uri

dispatched

routed

## Зміст

-   [Yaf\_Request\_Http::\_\_construct](yaf-request-http.construct.md) \- Конструктор класу Yaf\_Request\_Http
-   [Yaf\_Request\_Http::get](yaf-request-http.get.md)— Отримує змінну від клієнта
-   [Yaf\_Request\_Http::getCookie](yaf-request-http.getcookie.md)— Отримує змінну Cookie
-   [Yaf\_Request\_Http::getFiles](yaf-request-http.getfiles.md) \- Призначення getFiles
-   [Yaf\_Request\_Http::getPost](yaf-request-http.getpost.md)— Отримує змінну POST
-   [Yaf\_Request\_Http::getQuery](yaf-request-http.getquery.md)— Отримує параметр запиту
-   [Yaf\_Request\_Http::getRaw](yaf-request-http.getraw.md)— Отримує необроблене тіло запиту
-   [Yaf\_Request\_Http::getRequest](yaf-request-http.getrequest.md) \- Призначення getRequest
-   [Yaf\_Request\_Http::isXmlHttpRequest](yaf-request-http.isxmlhttprequest.md)— Визначає, чи є запит Ajax-запитом

---
navigation:
  - yaf-request-http.isxmlhttprequest.md: '« Yaf\_Request\_Http::isXmlHttpRequest'
  - yaf-request-simple.construct.md: 'Yaf\_Request\_Simple::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Request\_Simple
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Request\_Simple

(Yaf >=1.0.0)

## Вступ

**Yaf\_Request\_Simple** зазвичай використовується з метою тестування. Наприклад, для емуляції спеціальних запитів із режиму CLI.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Request_Simple
     

     
      extends
       Yaf_Request_Abstract
     
     {
    
    /* Константы */
    
     const
     string
      SCHEME_HTTP = http;

    const
     string
      SCHEME_HTTPS = https;


    /* Свойства */


    /* Методы */
    
   public __construct(    string $method = ?,    string $module = ?,    string $controller = ?,    string $action = ?,    array $params = ?)

    public get(): void
public getCookie(): void
public getFiles(): void
public getPost(): void
public getQuery(): void
public getRequest(): void
public isXmlHttpRequest(): void


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

## Обумовлені константи

**`Yaf_Request_Simple::SCHEME_HTTP`**

**`Yaf_Request_Simple::SCHEME_HTTPS`**

## Зміст

-   [Yaf\_Request\_Simple::\_\_construct](yaf-request-simple.construct.md) \- Конструктор класу Yaf\_Request\_Simple
-   [Yaf\_Request\_Simple::get](yaf-request-simple.get.md) \- Призначення get
-   [Yaf\_Request\_Simple::getCookie](yaf-request-simple.getcookie.md) \- Призначення getCookie
-   [Yaf\_Request\_Simple::getFiles](yaf-request-simple.getfiles.md) \- Призначення getFiles
-   [Yaf\_Request\_Simple::getPost](yaf-request-simple.getpost.md) \- Призначення getPost
-   [Yaf\_Request\_Simple::getQuery](yaf-request-simple.getquery.md) \- Призначення getQuery
-   [Yaf\_Request\_Simple::getRequest](yaf-request-simple.getrequest.md) \- Призначення getRequest
-   [Yaf\_Request\_Simple::isXmlHttpRequest](yaf-request-simple.isxmlhttprequest.md) \- Визначає, чи є запит AJAX-запитом

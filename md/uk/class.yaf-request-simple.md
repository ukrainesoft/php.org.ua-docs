---
navigation:
  - yaf-request-http.isxmlhttprequest.html: '« YafRequestHttp::isXmlHttpRequest'
  - yaf-request-simple.construct.html: 'YafRequestSimple::construct »'
  - index.html: PHP Manual
  - book.yaf.html: Yaf
title: Клас YafRequestSimple
---
# Клас YafRequestSimple

(Yaf >=1.0.0)

## Вступ

**YafRequestSimple** зазвичай використовується з метою тестування. Наприклад, для емуляції спеціальних запитів із режиму CLI.

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

метод

params

language

exception

baseuri

uri

dispatched

routed

## Обумовлені константи

**`Yaf_Request_Simple::SCHEME_HTTP`**

**`Yaf_Request_Simple::SCHEME_HTTPS`**

## Зміст

-   [YafRequestSimple::construct](yaf-request-simple.construct.html) - Конструктор класу YafRequestSimple
-   [YafRequestSimple::get](yaf-request-simple.get.html) - Призначення get
-   [YafRequestSimple::getCookie](yaf-request-simple.getcookie.html) - Призначення getCookie
-   [YafRequestSimple::getFiles](yaf-request-simple.getfiles.html) - Призначення getFiles
-   [YafRequestSimple::getPost](yaf-request-simple.getpost.html) - Призначення getPost
-   [YafRequestSimple::getQuery](yaf-request-simple.getquery.html) - Призначення getQuery
-   [YafRequestSimple::getRequest](yaf-request-simple.getrequest.html) - Призначення getRequest
-   [YafRequestSimple::isXmlHttpRequest](yaf-request-simple.isxmlhttprequest.html) - Визначає, чи є запит AJAX-запитом

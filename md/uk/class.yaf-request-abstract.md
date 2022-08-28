Клас YafRequestAbstract

-   [« Yaf\_Registry::set](yaf-registry.set.html)
    
-   [Yaf\_Request\_Abstract::clearParams »](yaf-request-abstract.clearparams.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRequestAbstract
    

# Клас YafRequestAbstract

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Request_Abstract
     
     {
    
    /* Константы */
    
     const
     string
      SCHEME_HTTP = http;

    const
     string
      SCHEME_HTTPS = https;


    /* Свойства */
    public
      $module;

    public
      $controller;

    public
      $action;

    public
      $method;

    protected
      $params;

    protected
      $language;

    protected
      $_exception;

    protected
      $_base_uri;

    protected
      $uri;

    protected
      $dispatched;

    protected
      $routed;



    /* Методы */
    
   public clearParams(): bool
public getActionName(): void
public getBaseUri(): void
public getControllerName(): void
public getEnv(string $name, string $default = ?): void
public getException(): void
public getLanguage(): void
public getMethod(): string
public getModuleName(): void
public getParam(string $name, string $default = ?): mixed
public getParams(): array
public getRequestUri(): void
public getServer(string $name, string $default = ?): void
public isCli(): bool
public isDispatched(): bool
public isGet(): bool
public isHead(): bool
public isOptions(): bool
public isPost(): bool
public isPut(): bool
public isRouted(): bool
public isXmlHttpRequest(): bool
public setActionName(string $action, bool $format_name = true): void
public setBaseUri(string $uir): bool
public setControllerName(string $controller, bool $format_name = true): void
public setDispatched(): void
public setModuleName(string $module, bool $format_name = true): void
public setParam(string $name, string $value = ?): bool
public setRequestUri(string $uir): void
public setRouted(string $flag = ?): void

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

**`Yaf_Request_Abstract::SCHEME_HTTP`**

**`Yaf_Request_Abstract::SCHEME_HTTPS`**

## Зміст

-   [Yaf\_Request\_Abstract::clearParams](yaf-request-abstract.clearparams.html) — Видаляє всі параметри
-   [Yaf\_Request\_Abstract::getActionName](yaf-request-abstract.getactionname.html) — Призначення getActionName
-   [Yaf\_Request\_Abstract::getBaseUri](yaf-request-abstract.getbaseuri.html) - Призначення getBaseUri
-   [Yaf\_Request\_Abstract::getControllerName](yaf-request-abstract.getcontrollername.html) — Призначення getControllerName
-   [Yaf\_Request\_Abstract::getEnv](yaf-request-abstract.getenv.html) — Отримує змінну ENV
-   [Yaf\_Request\_Abstract::getException](yaf-request-abstract.getexception.html) - Призначення getException
-   [Yaf\_Request\_Abstract::getLanguage](yaf-request-abstract.getlanguage.html) — Отримує кращу мову клієнта
-   [Yaf\_Request\_Abstract::getMethod](yaf-request-abstract.getmethod.html) — Отримує метод запиту
-   [Yaf\_Request\_Abstract::getModuleName](yaf-request-abstract.getmodulename.html) — Призначення getModuleName
-   [Yaf\_Request\_Abstract::getParam](yaf-request-abstract.getparam.html) — Отримує параметр дзвінка
-   [Yaf\_Request\_Abstract::getParams](yaf-request-abstract.getparams.html) — Отримує всі параметри дзвінка
-   [Yaf\_Request\_Abstract::getRequestUri](yaf-request-abstract.getrequesturi.html) - Призначення getRequestUri
-   [Yaf\_Request\_Abstract::getServer](yaf-request-abstract.getserver.html) — Отримує змінну SERVER
-   [Yaf\_Request\_Abstract::isCli](yaf-request-abstract.iscli.html) — Визначає, чи є запит CLI-запитом
-   [Yaf\_Request\_Abstract::isDispatched](yaf-request-abstract.isdispatched.html) — Визначає, чи надіслано запит.
-   [Yaf\_Request\_Abstract::isGet](yaf-request-abstract.isget.html) - Визначає, чи є запит GET-запитом
-   [Yaf\_Request\_Abstract::isHead](yaf-request-abstract.ishead.html) - Визначає, чи є запит HEAD-запитом
-   [Yaf\_Request\_Abstract::isOptions](yaf-request-abstract.isoptions.html) — Визначає, чи є запит OPTIONS-запитом
-   [Yaf\_Request\_Abstract::isPost](yaf-request-abstract.ispost.html) — Визначає, чи запит POST-запитом.
-   [Yaf\_Request\_Abstract::isPut](yaf-request-abstract.isput.html) - Визначає, чи є запит PUT-запитом
-   [Yaf\_Request\_Abstract::isRouted](yaf-request-abstract.isrouted.html) — Визначає, чи запит надіслано
-   [Yaf\_Request\_Abstract::isXmlHttpRequest](yaf-request-abstract.isxmlhttprequest.html) - Визначає, чи є запит AJAX-запитом
-   [Yaf\_Request\_Abstract::setActionName](yaf-request-abstract.setactionname.html) - Встановлює ім'я дії
-   [Yaf\_Request\_Abstract::setBaseUri](yaf-request-abstract.setbaseuri.html) - Встановлює базовий URI
-   [Yaf\_Request\_Abstract::setControllerName](yaf-request-abstract.setcontrollername.html) - Встановлює ім'я контролера
-   [Yaf\_Request\_Abstract::setDispatched](yaf-request-abstract.setdispatched.html) - Призначення setDispatched
-   [Yaf\_Request\_Abstract::setModuleName](yaf-request-abstract.setmodulename.html) - Встановлює ім'я модуля
-   [Yaf\_Request\_Abstract::setParam](yaf-request-abstract.setparam.html) — Встановлює дзвінок для запиту
-   [Yaf\_Request\_Abstract::setRequestUri](yaf-request-abstract.setrequesturi.html) - Призначення setRequestUri
-   [Yaf\_Request\_Abstract::setRouted](yaf-request-abstract.setrouted.html) — Призначення setRouted
---
navigation:
  - yaf-registry.set.html: '« YafRegistry::set'
  - yaf-request-abstract.clearparams.html: 'YafRequestAbstract::clearParams »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafRequestAbstract
---
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

-   [YafRequestAbstract::clearParams](yaf-request-abstract.clearparams.md) — Видаляє всі параметри
-   [YafRequestAbstract::getActionName](yaf-request-abstract.getactionname.md) — Призначення getActionName
-   [YafRequestAbstract::getBaseUri](yaf-request-abstract.getbaseuri.md) - Призначення getBaseUri
-   [YafRequestAbstract::getControllerName](yaf-request-abstract.getcontrollername.md) — Призначення getControllerName
-   [YafRequestAbstract::getEnv](yaf-request-abstract.getenv.md) — Отримує змінну ENV
-   [YafRequestAbstract::getException](yaf-request-abstract.getexception.md) - Призначення getException
-   [YafRequestAbstract::getLanguage](yaf-request-abstract.getlanguage.md) — Отримує кращу мову клієнта
-   [YafRequestAbstract::getMethod](yaf-request-abstract.getmethod.md) — Отримує метод запиту
-   [YafRequestAbstract::getModuleName](yaf-request-abstract.getmodulename.md) — Призначення getModuleName
-   [YafRequestAbstract::getParam](yaf-request-abstract.getparam.md) — Отримує параметр дзвінка
-   [YafRequestAbstract::getParams](yaf-request-abstract.getparams.md) — Отримує всі параметри дзвінка
-   [YafRequestAbstract::getRequestUri](yaf-request-abstract.getrequesturi.md) - Призначення getRequestUri
-   [YafRequestAbstract::getServer](yaf-request-abstract.getserver.md) — Отримує змінну SERVER
-   [YafRequestAbstract::isCli](yaf-request-abstract.iscli.md) — Визначає, чи є запит CLI-запитом
-   [YafRequestAbstract::isDispatched](yaf-request-abstract.isdispatched.md) — Визначає, чи надіслано запит.
-   [YafRequestAbstract::isGet](yaf-request-abstract.isget.md) - Визначає, чи є запит GET-запитом
-   [YafRequestAbstract::isHead](yaf-request-abstract.ishead.md) - Визначає, чи є запит HEAD-запитом
-   [YafRequestAbstract::isOptions](yaf-request-abstract.isoptions.md) — Визначає, чи є запит OPTIONS-запитом
-   [YafRequestAbstract::isPost](yaf-request-abstract.ispost.md) — Визначає, чи запит POST-запитом.
-   [YafRequestAbstract::isPut](yaf-request-abstract.isput.md) - Визначає, чи є запит PUT-запитом
-   [YafRequestAbstract::isRouted](yaf-request-abstract.isrouted.md) — Визначає, чи запит надіслано
-   [YafRequestAbstract::isXmlHttpRequest](yaf-request-abstract.isxmlhttprequest.md) - Визначає, чи є запит AJAX-запитом
-   [YafRequestAbstract::setActionName](yaf-request-abstract.setactionname.md) - Встановлює ім'я дії
-   [YafRequestAbstract::setBaseUri](yaf-request-abstract.setbaseuri.md) - Встановлює базовий URI
-   [YafRequestAbstract::setControllerName](yaf-request-abstract.setcontrollername.md) - Встановлює ім'я контролера
-   [YafRequestAbstract::setDispatched](yaf-request-abstract.setdispatched.md) - Призначення setDispatched
-   [YafRequestAbstract::setModuleName](yaf-request-abstract.setmodulename.md) - Встановлює ім'я модуля
-   [YafRequestAbstract::setParam](yaf-request-abstract.setparam.md) — Встановлює дзвінок для запиту
-   [YafRequestAbstract::setRequestUri](yaf-request-abstract.setrequesturi.md) - Призначення setRequestUri
-   [YafRequestAbstract::setRouted](yaf-request-abstract.setrouted.md) — Призначення setRouted

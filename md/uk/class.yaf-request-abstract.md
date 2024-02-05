---
navigation:
  - yaf-registry.set.md: '« Yaf\_Registry::set'
  - yaf-request-abstract.clearparams.md: 'Yaf\_Request\_Abstract::clearParams »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Request\_Abstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Request\_Abstract

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

method

params

language

\_exception

\_base\_uri

uri

dispatched

routed

## Обумовлені константи

**`Yaf_Request_Abstract::SCHEME_HTTP`**

**`Yaf_Request_Abstract::SCHEME_HTTPS`**

## Зміст

-   [Yaf\_Request\_Abstract::clearParams](yaf-request-abstract.clearparams.md)— Видаляє всі параметри
-   [Yaf\_Request\_Abstract::getActionName](yaf-request-abstract.getactionname.md)— Призначення getActionName
-   [Yaf\_Request\_Abstract::getBaseUri](yaf-request-abstract.getbaseuri.md) \- Призначення getBaseUri
-   [Yaf\_Request\_Abstract::getControllerName](yaf-request-abstract.getcontrollername.md)— Призначення getControllerName
-   [Yaf\_Request\_Abstract::getEnv](yaf-request-abstract.getenv.md)— Отримує змінну ENV
-   [Yaf\_Request\_Abstract::getException](yaf-request-abstract.getexception.md) \- Призначення getException
-   [Yaf\_Request\_Abstract::getLanguage](yaf-request-abstract.getlanguage.md)— Отримує кращу мову клієнта
-   [Yaf\_Request\_Abstract::getMethod](yaf-request-abstract.getmethod.md)— Отримує метод запиту
-   [Yaf\_Request\_Abstract::getModuleName](yaf-request-abstract.getmodulename.md)— Призначення getModuleName
-   [Yaf\_Request\_Abstract::getParam](yaf-request-abstract.getparam.md)— Отримує параметр дзвінка
-   [Yaf\_Request\_Abstract::getParams](yaf-request-abstract.getparams.md)— Отримує всі параметри дзвінка
-   [Yaf\_Request\_Abstract::getRequestUri](yaf-request-abstract.getrequesturi.md) \- Призначення getRequestUri
-   [Yaf\_Request\_Abstract::getServer](yaf-request-abstract.getserver.md)— Отримує змінну SERVER
-   [Yaf\_Request\_Abstract::isCli](yaf-request-abstract.iscli.md)— Визначає, чи є запит CLI-запитом
-   [Yaf\_Request\_Abstract::isDispatched](yaf-request-abstract.isdispatched.md)— Визначає, чи надіслано запит.
-   [Yaf\_Request\_Abstract::isGet](yaf-request-abstract.isget.md) \- Визначає, чи є запит GET-запитом
-   [Yaf\_Request\_Abstract::isHead](yaf-request-abstract.ishead.md) \- Визначає, чи є запит HEAD-запитом
-   [Yaf\_Request\_Abstract::isOptions](yaf-request-abstract.isoptions.md)— Визначає, чи є запит OPTIONS-запитом
-   [Yaf\_Request\_Abstract::isPost](yaf-request-abstract.ispost.md)— Визначає, чи запит POST-запитом.
-   [Yaf\_Request\_Abstract::isPut](yaf-request-abstract.isput.md) \- Визначає, чи є запит PUT-запитом
-   [Yaf\_Request\_Abstract::isRouted](yaf-request-abstract.isrouted.md)— Визначає, чи запит надіслано
-   [Yaf\_Request\_Abstract::isXmlHttpRequest](yaf-request-abstract.isxmlhttprequest.md) \- Визначає, чи є запит AJAX-запитом
-   [Yaf\_Request\_Abstract::setActionName](yaf-request-abstract.setactionname.md) \- Встановлює ім'я дії
-   [Yaf\_Request\_Abstract::setBaseUri](yaf-request-abstract.setbaseuri.md) \- Встановлює базовий URI
-   [Yaf\_Request\_Abstract::setControllerName](yaf-request-abstract.setcontrollername.md) \- Встановлює ім'я контролера
-   [Yaf\_Request\_Abstract::setDispatched](yaf-request-abstract.setdispatched.md) \- Призначення setDispatched
-   [Yaf\_Request\_Abstract::setModuleName](yaf-request-abstract.setmodulename.md) \- Встановлює ім'я модуля
-   [Yaf\_Request\_Abstract::setParam](yaf-request-abstract.setparam.md)— Встановлює дзвінок для запиту
-   [Yaf\_Request\_Abstract::setRequestUri](yaf-request-abstract.setrequesturi.md) \- Призначення setRequestUri
-   [Yaf\_Request\_Abstract::setRouted](yaf-request-abstract.setrouted.md)— Призначення setRouted

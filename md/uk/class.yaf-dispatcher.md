---
navigation:
  - class.yaf-bootstrap-abstract.html: « YafBootstrapAbstract
  - yaf-dispatcher.autorender.html: 'YafDispatcher::autoRender »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafDispatcher
---
# Клас YafDispatcher

(Yaf >=1.0.0)

## Вступ

**YafDispatcher** призначений для ініціалізації оточення запиту, маршрутизації вхідного запиту та подальшого відправлення будь-яких виявлених завдань; агрегує всі відповіді та повертає їх після завершення процесу.

**YafDispatcher** реалізує шаблон проектування Singleton, це означає, що тільки один екземпляр класу може бути доступний у будь-який час. Це дозволяє йому також виступати в якості реєстру, в який інші об'єкти в процесі диспетчеризації можуть підтягуватися.

## Огляд класів

```classsynopsis


    
    
     
      final
      class Yaf_Dispatcher
     
     {
    
    /* Свойства */
    
     protected
      $_router;

    protected
      $_view;

    protected
      $_request;

    protected
      $_plugins;

    protected
     static
      $_instance;

    protected
      $_auto_render;

    protected
      $_return_response;

    protected
      $_instantly_flush;

    protected
      $_default_module;

    protected
      $_default_controller;

    protected
      $_default_action;



    /* Методы */
    
   public __construct()

    public autoRender(bool $flag = ?): Yaf_Dispatcher
public catchException(bool $flag = ?): Yaf_Dispatcher
public disableView(): bool
public dispatch(Yaf_Request_Abstract $request): Yaf_Response_Abstract
public enableView(): Yaf_Dispatcher
public flushInstantly(bool $flag = ?): Yaf_Dispatcher
public getApplication(): Yaf_Application
public getDefaultAction(): string
public getDefaultController(): string
public getDefaultModule(): string
public static getInstance(): Yaf_Dispatcher
public getRequest(): Yaf_Request_Abstract
public getRouter(): Yaf_Router
public initView(string $templates_dir, array $options = ?): Yaf_View_Interface
public registerPlugin(Yaf_Plugin_Abstract $plugin): Yaf_Dispatcher
public returnResponse(bool $flag): Yaf_Dispatcher
public setDefaultAction(string $action): Yaf_Dispatcher
public setDefaultController(string $controller): Yaf_Dispatcher
public setDefaultModule(string $module): Yaf_Dispatcher
public setErrorHandler(call $callback, int $error_types): Yaf_Dispatcher
public setRequest(Yaf_Request_Abstract $request): Yaf_Dispatcher
public setView(Yaf_View_Interface $view): Yaf_Dispatcher
public throwException(bool $flag = ?): Yaf_Dispatcher

   }
```

## Властивості

router

view

request

plugins

instance

autorender

returnresponse

instantlyflush

defaultmodule

defaultcontroller

defaultaction

## Зміст

-   [YafDispatcher::autoRender](yaf-dispatcher.autorender.md) — Включає/вимикає авторендеринг
-   [YafDispatcher::catchException](yaf-dispatcher.catchexception.md) — Включає/вимикає перехоплення винятків
-   [YafDispatcher::construct](yaf-dispatcher.construct.md) - Конструктор класу YafDispatcher
-   [YafDispatcher::disableView](yaf-dispatcher.disableview.md) — Вимикає механізм перегляду
-   [YafDispatcher::dispatch](yaf-dispatcher.dispatch.md) — Надсилає запит
-   [YafDispatcher::enableView](yaf-dispatcher.enableview.md) - Включає механізм перегляду
-   [YafDispatcher::flushInstantly](yaf-dispatcher.flushinstantly.md) — Вмикає/вимикає миттєве очищення
-   [YafDispatcher::getApplication](yaf-dispatcher.getapplication.md) — Отримує програму
-   [YafDispatcher::getDefaultAction](yaf-dispatcher.getdefaultaction.md) — Отримує ім'я стандартної дії
-   [YafDispatcher::getDefaultController](yaf-dispatcher.getdefaultcontroller.md) — Отримує ім'я контролера за умовчанням
-   [YafDispatcher::getDefaultModule](yaf-dispatcher.getdefaultmodule.md) — Отримує ім'я модуля за замовчуванням
-   [YafDispatcher::getInstance](yaf-dispatcher.getinstance.md) — Отримує екземпляр диспетчера
-   [YafDispatcher::getRequest](yaf-dispatcher.getrequest.md) — Отримує екземпляр запиту
-   [YafDispatcher::getRouter](yaf-dispatcher.getrouter.md) — Отримує екземпляр маршрутизатора
-   [YafDispatcher::initView](yaf-dispatcher.initview.md) — Ініціалізує виставу та повертає її
-   [YafDispatcher::registerPlugin](yaf-dispatcher.registerplugin.md) - Реєструє плагін
-   [YafDispatcher::returnResponse](yaf-dispatcher.returnresponse.md) — Призначення returnResponse
-   [YafDispatcher::setDefaultAction](yaf-dispatcher.setdefaultaction.md) — Змінює ім'я стандартної дії
-   [YafDispatcher::setDefaultController](yaf-dispatcher.setdefaultcontroller.md) - Змінює ім'я контролера за умовчанням
-   [YafDispatcher::setDefaultModule](yaf-dispatcher.setdefaultmodule.md) — Змінює стандартне ім'я модуля
-   [YafDispatcher::setErrorHandler](yaf-dispatcher.seterrorhandler.md) - Встановлює обробник помилок
-   [YafDispatcher::setRequest](yaf-dispatcher.setrequest.md) - Призначення setRequest
-   [YafDispatcher::setView](yaf-dispatcher.setview.md) — Встановлює користувальницький механізм відображення
-   [YafDispatcher::throwException](yaf-dispatcher.throwexception.md) — Вмикає/вимикає викидання винятків

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

-   [YafDispatcher::autoRender](yaf-dispatcher.autorender.html) — Включає/вимикає авторендеринг
-   [YafDispatcher::catchException](yaf-dispatcher.catchexception.html) — Включає/вимикає перехоплення винятків
-   [YafDispatcher::construct](yaf-dispatcher.construct.html) - Конструктор класу YafDispatcher
-   [YafDispatcher::disableView](yaf-dispatcher.disableview.html) — Вимикає механізм перегляду
-   [YafDispatcher::dispatch](yaf-dispatcher.dispatch.html) — Надсилає запит
-   [YafDispatcher::enableView](yaf-dispatcher.enableview.html) - Включає механізм перегляду
-   [YafDispatcher::flushInstantly](yaf-dispatcher.flushinstantly.html) — Вмикає/вимикає миттєве очищення
-   [YafDispatcher::getApplication](yaf-dispatcher.getapplication.html) — Отримує програму
-   [YafDispatcher::getDefaultAction](yaf-dispatcher.getdefaultaction.html) — Отримує ім'я стандартної дії
-   [YafDispatcher::getDefaultController](yaf-dispatcher.getdefaultcontroller.html) — Отримує ім'я контролера за умовчанням
-   [YafDispatcher::getDefaultModule](yaf-dispatcher.getdefaultmodule.html) — Отримує ім'я модуля за замовчуванням
-   [YafDispatcher::getInstance](yaf-dispatcher.getinstance.html) — Отримує екземпляр диспетчера
-   [YafDispatcher::getRequest](yaf-dispatcher.getrequest.html) — Отримує екземпляр запиту
-   [YafDispatcher::getRouter](yaf-dispatcher.getrouter.html) — Отримує екземпляр маршрутизатора
-   [YafDispatcher::initView](yaf-dispatcher.initview.html) — Ініціалізує виставу та повертає її
-   [YafDispatcher::registerPlugin](yaf-dispatcher.registerplugin.html) - Реєструє плагін
-   [YafDispatcher::returnResponse](yaf-dispatcher.returnresponse.html) — Призначення returnResponse
-   [YafDispatcher::setDefaultAction](yaf-dispatcher.setdefaultaction.html) — Змінює ім'я стандартної дії
-   [YafDispatcher::setDefaultController](yaf-dispatcher.setdefaultcontroller.html) - Змінює ім'я контролера за умовчанням
-   [YafDispatcher::setDefaultModule](yaf-dispatcher.setdefaultmodule.html) — Змінює стандартне ім'я модуля
-   [YafDispatcher::setErrorHandler](yaf-dispatcher.seterrorhandler.html) - Встановлює обробник помилок
-   [YafDispatcher::setRequest](yaf-dispatcher.setrequest.html) - Призначення setRequest
-   [YafDispatcher::setView](yaf-dispatcher.setview.html) — Встановлює користувальницький механізм відображення
-   [YafDispatcher::throwException](yaf-dispatcher.throwexception.html) — Вмикає/вимикає викидання винятків

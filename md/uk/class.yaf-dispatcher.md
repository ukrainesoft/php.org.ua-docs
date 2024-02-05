---
navigation:
  - class.yaf-bootstrap-abstract.md: « Yaf\_Bootstrap\_Abstract
  - yaf-dispatcher.autorender.md: 'Yaf\_Dispatcher::autoRender »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Dispatcher
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Dispatcher

(Yaf >=1.0.0)

## Вступ

**Yaf\_Dispatcher** призначений для ініціалізації оточення запиту, маршрутизації вхідного запиту та подальшого відправлення будь-яких виявлених завдань; агрегує всі відповіді та повертає їх після завершення процесу.

**Yaf\_Dispatcher** реалізує шаблон проектування Singleton, це означає, що тільки один екземпляр класу може бути доступний у будь-який час. Це дозволяє йому також виступати в якості реєстру, в який інші об'єкти в процесі диспетчеризації можуть підтягуватися.

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

\_router

\_view

\_request

\_plugins

\_instance

\_auto\_render

\_return\_response

\_instantly\_flush

\_default\_module

\_default\_controller

\_default\_action

## Зміст

-   [Yaf\_Dispatcher::autoRender](yaf-dispatcher.autorender.md)— Включає/вимикає авторендеринг
-   [Yaf\_Dispatcher::catchException](yaf-dispatcher.catchexception.md)— Включає/вимикає перехоплення винятків
-   [Yaf\_Dispatcher::\_\_construct](yaf-dispatcher.construct.md) \- Конструктор класу Yaf\_Dispatcher
-   [Yaf\_Dispatcher::disableView](yaf-dispatcher.disableview.md)— Вимикає механізм перегляду
-   [Yaf\_Dispatcher::dispatch](yaf-dispatcher.dispatch.md)— Надсилає запит
-   [Yaf\_Dispatcher::enableView](yaf-dispatcher.enableview.md) \- Включає механізм перегляду
-   [Yaf\_Dispatcher::flushInstantly](yaf-dispatcher.flushinstantly.md)— Вмикає/вимикає миттєве очищення
-   [Yaf\_Dispatcher::getApplication](yaf-dispatcher.getapplication.md)— Отримує програму
-   [Yaf\_Dispatcher::getDefaultAction](yaf-dispatcher.getdefaultaction.md)— Отримує ім'я стандартної дії
-   [Yaf\_Dispatcher::getDefaultController](yaf-dispatcher.getdefaultcontroller.md)— Отримує ім'я контролера за умовчанням
-   [Yaf\_Dispatcher::getDefaultModule](yaf-dispatcher.getdefaultmodule.md)— Отримує ім'я модуля за замовчуванням
-   [Yaf\_Dispatcher::getInstance](yaf-dispatcher.getinstance.md)— Отримує екземпляр диспетчера
-   [Yaf\_Dispatcher::getRequest](yaf-dispatcher.getrequest.md)— Отримує екземпляр запиту
-   [Yaf\_Dispatcher::getRouter](yaf-dispatcher.getrouter.md)— Отримує екземпляр маршрутизатора
-   [Yaf\_Dispatcher::initView](yaf-dispatcher.initview.md)— Ініціалізує виставу та повертає її
-   [Yaf\_Dispatcher::registerPlugin](yaf-dispatcher.registerplugin.md) \- Реєструє плагін
-   [Yaf\_Dispatcher::returnResponse](yaf-dispatcher.returnresponse.md)— Призначення returnResponse
-   [Yaf\_Dispatcher::setDefaultAction](yaf-dispatcher.setdefaultaction.md)— Змінює ім'я стандартної дії
-   [Yaf\_Dispatcher::setDefaultController](yaf-dispatcher.setdefaultcontroller.md) \- Змінює ім'я контролера за умовчанням
-   [Yaf\_Dispatcher::setDefaultModule](yaf-dispatcher.setdefaultmodule.md)— Змінює стандартне ім'я модуля
-   [Yaf\_Dispatcher::setErrorHandler](yaf-dispatcher.seterrorhandler.md) \- Встановлює обробник помилок
-   [Yaf\_Dispatcher::setRequest](yaf-dispatcher.setrequest.md) \- Призначення setRequest
-   [Yaf\_Dispatcher::setView](yaf-dispatcher.setview.md)— Встановлює користувальницький механізм відображення
-   [Yaf\_Dispatcher::throwException](yaf-dispatcher.throwexception.md)— Вмикає/вимикає викидання винятків

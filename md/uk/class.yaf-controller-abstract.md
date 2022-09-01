---
navigation:
  - yaf-config-simple.valid.html: '« YafConfigSimple::valid'
  - yaf-controller-abstract.construct.html: 'YafControllerAbstract::construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafControllerAbstract
---
# Клас YafControllerAbstract

(Yaf >=1.0.0)

## Вступ

**YafControllerAbstract** це серце системи Yaf. MVC розшифровується як Model-View-Controller і є шаблоном проектування, призначений для відділення логіки програми від логіки відображення

Кожен контролер повинен успадковувати **YafControllerAbstract**

Ви знайдете, що не можете визначити функцію construct для свого користувача контролера, тому **YafControllerAbstract** надає

Якщо ви визначили метод init() у своєму контролері користувача, він буде викликатися доти, поки буде створено екземпляр контролера.

У дії під час надходження запиту може бути аргументи. Якщо в параметрах запиту є та сама змінна імені ([YafRequestAbstract::getParam()](yaf-request-abstract.getparam.html)) після перенаправлення, Yaf передасть їх методу дії ([YafActionAbstract::execute()](yaf-action-abstract.execute.md)

> **Зауваження**
> 
> Аргументи витягуються безпосередньо без фільтрації, перед використанням слід ретельно обробити.

## Огляд класів

```classsynopsis


    
    
     
      abstract
      class Yaf_Controller_Abstract
     
     {
    
    /* Свойства */
    
     public
      $actions;

    protected
      $_module;

    protected
      $_name;

    protected
      $_request;

    protected
      $_response;

    protected
      $_invoke_args;

    protected
      $_view;



    /* Методы */
    
   final private __construct()

    protected display(string $tpl, array $parameters = ?): bool
public forward(string $action, array $paramters = ?): bool
public getInvokeArg(string $name): void
public getInvokeArgs(): void
public getModuleName(): string
public getName(): string
public getRequest(): Yaf_Request_Abstract
public getResponse(): Yaf_Response_Abstract
public getView(): Yaf_View_Interface
public getViewpath(): string
public init(): void
public initView(array $options = ?): void
public redirect(string $url): bool
protected render(string $tpl, array $parameters = ?): string
public setViewpath(string $view_directory): void

   }
```

## Властивості

actions

Ви також можете визначити метод дії в окремому скрипті PHP, використовуючи цю властивість і [YafActionAbstract](class.yaf-action-abstract.md)

**Приклад #1 Визначення дії в окремому файлі**

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    protected $actions = array(
        /** теперь dummyAction определяется в отдельном файле */
        "dummy" => "actions/Dummy_action.php",
    );

    /* у метода действия могут быть аргументы */
    public function indexAction($name, $id) {
       /* $name и $id небезопасные необработанные данные */
       assert($name == $this->getRequest()->getParam("name"));
       assert($id   == $this->_request->getParam("id"));
    }
}
?>
```

**Приклад #2 Dummyaction.php**

```php
<?php
class DummyAction extends Yaf_Action_Abstract {
    /* класс действия должен определить этот метод как точку входа */
    public function execute() {
    }
}
?>
```

module

ім'я модуля

name

ім'я контролера

request

поточний об'єкт запиту

response

поточний об'єкт відповіді

invokeargs

view

об'єкт движка відображення

## Зміст

-   [YafControllerAbstract::construct](yaf-controller-abstract.construct.md) - Конструктор класу YafControllerAbstract
-   [YafControllerAbstract::display](yaf-controller-abstract.display.md) - Призначення display
-   [YafControllerAbstract::forward](yaf-controller-abstract.forward.md) — Переходить до іншої дії
-   [YafControllerAbstract::getInvokeArg](yaf-controller-abstract.getinvokearg.md) — Призначення getInvokeArg
-   [YafControllerAbstract::getInvokeArgs](yaf-controller-abstract.getinvokeargs.md) — Призначення getInvokeArgs
-   [YafControllerAbstract::getModuleName](yaf-controller-abstract.getmodulename.md) — Отримує ім'я модуля
-   [YafControllerAbstract::getName](yaf-controller-abstract.getname.md) — Отримує своє ім'я
-   [YafControllerAbstract::getRequest](yaf-controller-abstract.getrequest.md) — Отримує поточний об'єкт запиту
-   [YafControllerAbstract::getResponse](yaf-controller-abstract.getresponse.md) — Отримує поточний об'єкт відповіді
-   [YafControllerAbstract::getView](yaf-controller-abstract.getview.md) — Отримує двигун відображення
-   [YafControllerAbstract::getViewpath](yaf-controller-abstract.getviewpath.md) - Призначення getViewpath
-   [YafControllerAbstract::init](yaf-controller-abstract.init.md) - Ініціалізатор контролера
-   [YafControllerAbstract::initView](yaf-controller-abstract.initview.md) - Призначення initView
-   [YafControllerAbstract::redirect](yaf-controller-abstract.redirect.md) — Перенаправляє на URL
-   [YafControllerAbstract::render](yaf-controller-abstract.render.md) — Відображає шаблон представлення
-   [YafControllerAbstract::setViewpath](yaf-controller-abstract.setviewpath.md) - Призначення setViewpath

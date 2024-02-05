---
navigation:
  - yaf-config-simple.valid.md: '« Yaf\_Config\_Simple::valid'
  - yaf-controller-abstract.construct.md: 'Yaf\_Controller\_Abstract::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Controller\_Abstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Controller\_Abstract

(Yaf >=1.0.0)

## Вступ

**Yaf\_Controller\_Abstract** це серце системи Yaf. MVC розшифровується як Model-View-Controller і є шаблоном проектування, призначений для відділення логіки програми від логіки відображення

Кожен контролер повинен успадковувати **Yaf\_Controller\_Abstract**

Ви знайдете, що не можете визначити функцію \_\_construct для свого користувача контролера, тому **Yaf\_Controller\_Abstract**предоставляет

Якщо ви визначили метод init() у своєму контролері користувача, він буде викликатися доти, поки буде створено екземпляр контролера.

У дії під час надходження запиту може бути аргументи. Якщо в параметрах запиту є та сама змінна імені ([Yaf\_Request\_Abstract::getParam()](yaf-request-abstract.getparam.md)) після перенаправлення, Yaf передасть їх методу дії ([Yaf\_Action\_Abstract::execute()](yaf-action-abstract.execute.md)

> **Зауваження** :
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

Ви також можете визначити метод дії в окремому скрипті PHP, використовуючи цю властивість і [Yaf\_Action\_Abstract](class.yaf-action-abstract.md)

**Приклад #1 Визначення дії в окремому файлі**

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    protected $actions = array(
        /** теперь dummyAction определяется в отдельном файле */
        "dummy" => "actions/Dummy_action.php",
    );

    /* у метода действия могут быть аргументы */
    public function indexAction($name, $id) {
       /* $name и $id небезопасные необработанные данные */
       assert($name == $this->getRequest()->getParam("name"));
       assert($id   == $this->_request->getParam("id"));
    }
}
?>
```

**Приклад #2 Dummy\_action.php**

```php
<?php
class DummyAction extends Yaf_Action_Abstract {
    /* класс действия должен определить этот метод как точку входа */
    public function execute() {
    }
}
?>
```

\_module

ім'я модуля

\_name

ім'я контролера

\_request

поточний об'єкт запиту

\_response

поточний об'єкт відповіді

\_invoke\_args

\_view

об'єкт движка відображення

## Зміст

-   [Yaf\_Controller\_Abstract::\_\_construct](yaf-controller-abstract.construct.md) \- Конструктор класу Yaf\_Controller\_Abstract
-   [Yaf\_Controller\_Abstract::display](yaf-controller-abstract.display.md) \- Призначення display
-   [Yaf\_Controller\_Abstract::forward](yaf-controller-abstract.forward.md)— Переходить до іншої дії
-   [Yaf\_Controller\_Abstract::getInvokeArg](yaf-controller-abstract.getinvokearg.md)— Призначення getInvokeArg
-   [Yaf\_Controller\_Abstract::getInvokeArgs](yaf-controller-abstract.getinvokeargs.md)— Призначення getInvokeArgs
-   [Yaf\_Controller\_Abstract::getModuleName](yaf-controller-abstract.getmodulename.md)— Отримує ім'я модуля
-   [Yaf\_Controller\_Abstract::getName](yaf-controller-abstract.getname.md)— Отримує своє ім'я
-   [Yaf\_Controller\_Abstract::getRequest](yaf-controller-abstract.getrequest.md)— Отримує поточний об'єкт запиту
-   [Yaf\_Controller\_Abstract::getResponse](yaf-controller-abstract.getresponse.md)— Отримує поточний об'єкт відповіді
-   [Yaf\_Controller\_Abstract::getView](yaf-controller-abstract.getview.md)— Отримує двигун відображення
-   [Yaf\_Controller\_Abstract::getViewpath](yaf-controller-abstract.getviewpath.md) \- Призначення getViewpath
-   [Yaf\_Controller\_Abstract::init](yaf-controller-abstract.init.md) \- Ініціалізатор контролера
-   [Yaf\_Controller\_Abstract::initView](yaf-controller-abstract.initview.md) \- Призначення initView
-   [Yaf\_Controller\_Abstract::redirect](yaf-controller-abstract.redirect.md)— Перенаправляє на URL
-   [Yaf\_Controller\_Abstract::render](yaf-controller-abstract.render.md)— Відображає шаблон представлення
-   [Yaf\_Controller\_Abstract::setViewpath](yaf-controller-abstract.setviewpath.md) \- Призначення setViewpath

Клас YafControllerAbstract

-   [« Yaf\_Config\_Simple::valid](yaf-config-simple.valid.html)
    
-   [Yaf\_Controller\_Abstract::\_\_construct »](yaf-controller-abstract.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafControllerAbstract
    

# Клас YafControllerAbstract

(Yaf >=1.0.0)

## Вступ

**YafControllerAbstract** це серце системи Yaf. MVC розшифровується як Model-View-Controller і є шаблоном проектування, призначений для відділення логіки програми від логіки відображення

Кожен контролер повинен успадковувати **YafControllerAbstract**

Ви знайдете, що не можете визначити функцію construct для свого користувача контролера, тому **YafControllerAbstract** надає

Якщо ви визначили метод init() у своєму контролері користувача, він буде викликатися доти, поки буде створено екземпляр контролера.

У дії під час надходження запиту може бути аргументи. Якщо в параметрах запиту є та сама змінна імені ([Yaf\_Request\_Abstract::getParam()](yaf-request-abstract.getparam.html)) після перенаправлення, Yaf передасть їх методу дії ([Yaf\_Action\_Abstract::execute()](yaf-action-abstract.execute.html)

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

Ви також можете визначити метод дії в окремому скрипті PHP, використовуючи цю властивість і [Yaf\_Action\_Abstract](class.yaf-action-abstract.html)

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

-   [Yaf\_Controller\_Abstract::\_\_construct](yaf-controller-abstract.construct.html) - Конструктор класу YafControllerAbstract
-   [Yaf\_Controller\_Abstract::display](yaf-controller-abstract.display.html) - Призначення display
-   [Yaf\_Controller\_Abstract::forward](yaf-controller-abstract.forward.html) — Переходить до іншої дії
-   [Yaf\_Controller\_Abstract::getInvokeArg](yaf-controller-abstract.getinvokearg.html) — Призначення getInvokeArg
-   [Yaf\_Controller\_Abstract::getInvokeArgs](yaf-controller-abstract.getinvokeargs.html) — Призначення getInvokeArgs
-   [Yaf\_Controller\_Abstract::getModuleName](yaf-controller-abstract.getmodulename.html) — Отримує ім'я модуля
-   [Yaf\_Controller\_Abstract::getName](yaf-controller-abstract.getname.html) — Отримує своє ім'я
-   [Yaf\_Controller\_Abstract::getRequest](yaf-controller-abstract.getrequest.html) — Отримує поточний об'єкт запиту
-   [Yaf\_Controller\_Abstract::getResponse](yaf-controller-abstract.getresponse.html) — Отримує поточний об'єкт відповіді
-   [Yaf\_Controller\_Abstract::getView](yaf-controller-abstract.getview.html) — Отримує двигун відображення
-   [Yaf\_Controller\_Abstract::getViewpath](yaf-controller-abstract.getviewpath.html) - Призначення getViewpath
-   [Yaf\_Controller\_Abstract::init](yaf-controller-abstract.init.html) - Ініціалізатор контролера
-   [Yaf\_Controller\_Abstract::initView](yaf-controller-abstract.initview.html) - Призначення initView
-   [Yaf\_Controller\_Abstract::redirect](yaf-controller-abstract.redirect.html) — Перенаправляє на URL
-   [Yaf\_Controller\_Abstract::render](yaf-controller-abstract.render.html) — Відображає шаблон представлення
-   [Yaf\_Controller\_Abstract::setViewpath](yaf-controller-abstract.setviewpath.html) - Призначення setViewpath
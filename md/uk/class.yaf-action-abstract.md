---
navigation:
  - yaf-controller-abstract.setviewpath.md: '« YafControllerAbstract::setViewpath'
  - yaf-action-abstract.execute.md: 'YafActionAbstract::execute »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafActionAbstract
---
# Клас YafActionAbstract

(Yaf >=1.0.0)

## Вступ

Дія повинна визначатися в окремому файлі в Yaf (див. [YafControllerAbstract](class.yaf-controller-abstract.md)). Також всі класи дії повинні розширювати **YafActionAbstract**

Так як необхідна точка входу, яку міг би використовувати Yaf, ви, у вашому класі, повинні реалізувати метод [YafActionAbstract::execute()](yaf-action-abstract.execute.md)

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Action_Abstract
     

     
      extends
       Yaf_Controller_Abstract
     
     {
    
    /* Свойства */
    
     protected
      $_controller;



    /* Методы */
    
   abstract publicexecute(mixed ...$args): mixed
publicgetController(): Yaf_Controller_Abstract
public getControllerName(): string


    /* Наследуемые методы */
    protected Yaf_Controller_Abstract::display(string $tpl, array $parameters = ?): bool
public Yaf_Controller_Abstract::forward(string $action, array $paramters = ?): bool
public Yaf_Controller_Abstract::getInvokeArg(string $name): void
public Yaf_Controller_Abstract::getInvokeArgs(): void
public Yaf_Controller_Abstract::getModuleName(): string
public Yaf_Controller_Abstract::getName(): string
public Yaf_Controller_Abstract::getRequest(): Yaf_Request_Abstract
public Yaf_Controller_Abstract::getResponse(): Yaf_Response_Abstract
public Yaf_Controller_Abstract::getView(): Yaf_View_Interface
public Yaf_Controller_Abstract::getViewpath(): string
public Yaf_Controller_Abstract::init(): void
public Yaf_Controller_Abstract::initView(array $options = ?): void
public Yaf_Controller_Abstract::redirect(string $url): bool
protected Yaf_Controller_Abstract::render(string $tpl, array $parameters = ?): string
public Yaf_Controller_Abstract::setViewpath(string $view_directory): void


   }
```

## Властивості

module

name

request

response

invokeargs

view

controller

## Зміст

-   [YafActionAbstract::execute](yaf-action-abstract.execute.md) - Точка входу для Action-класів
-   [YafActionAbstract::getController](yaf-action-abstract.getcontroller.md) - Отримати об'єкт контролер
-   [YafActionAbstract::getControllerName](yaf-controller-abstract.getcontrollername.md) — Отримує ім'я контролера

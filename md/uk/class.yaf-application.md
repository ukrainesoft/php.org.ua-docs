---
navigation:
  - yaf.appconfig.md: « Конфігурація програми
  - yaf-application.app.md: 'Yaf\_Application::app »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Application
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Application

(No version information available, might only be in Git)

## Вступ

[Yaf\_Application](class.yaf-application.md) забезпечує ініціалізацію об'єкта для додатків які надають ресурси, що використовуються, загальні та модульні bootstrap-класи та перевірки залежностей.

> **Зауваження** :
> 
> [Yaf\_Application](class.yaf-application.md) реалізує шаблоном singleton, та [Yaf\_Application](class.yaf-application.md) не може бути серіалізований або десеріалізований що викликає проблеми, коли ви намагаєтеся використовувати PHPUnit щоб написати деякі тести для Yaf.
> 
> Ви можете використовувати @backupGlobals анотації PHPUnit для контролю бекапів та операцій відновлення глобальних змінних. У такий спосіб можна вирішити цю проблему.

## Огляд класів

```classsynopsis



    
     
      final
      class Yaf_Application
     
     {

    /* Свойства */
    
     protected
      $config;

    protected
      $dispatcher;

    protected
     static
      $_app;

    protected
      $_modules;

    protected
      $_running;

    protected
      $_environ;



    /* Методы */
    
   public __construct(mixed $config, string $envrion = ?)

    public staticapp(): mixed
public bootstrap(Yaf_Bootstrap_Abstract $bootstrap = ?): void
public clearLastError(): Yaf_Application
public environ(): void
public execute(callable $entry, string ...$args): void
public getAppDirectory(): Yaf_Application
public getConfig(): Yaf_Config_Abstract
public getDispatcher(): Yaf_Dispatcher
public getLastErrorMsg(): string
public getLastErrorNo(): int
public getModules(): array
public run(): void
public setAppDirectory(string $directory): Yaf_Application

    public __destruct()

   }
```

## Властивості

config

dispatcher

\_app

\_modules

\_running

\_environ

## Зміст

-   [Yaf\_Application::app](yaf-application.app.md)— Вийняти екземпляр програми
-   [Yaf\_Application::bootstrap](yaf-application.bootstrap.md) \- Викликати bootstrap
-   [Yaf\_Application::clearLastError](yaf-application.clearlasterror.md)— Очищення інформації з останньої помилки
-   [Yaf\_Application::\_\_construct](yaf-application.construct.md) \- Конструктор класу Yaf\_Application
-   [Yaf\_Application::\_\_destruct](yaf-application.destruct.md) \- Деструктор Yaf\_Application
-   [Yaf\_Application::environ](yaf-application.environ.md)— Отримати значення оточення
-   [Yaf\_Application::execute](yaf-application.execute.md) \- Запустити callback-функцію
-   [Yaf\_Application::getAppDirectory](yaf-application.getappdirectory.md)— Отримати директорію програми
-   [Yaf\_Application::getConfig](yaf-application.getconfig.md)— Отримати екземпляр класу конфігурації
-   [Yaf\_Application::getDispatcher](yaf-application.getdispatcher.md) \- Отримати екземпляр класу Yaf\_Dispatcher
-   [Yaf\_Application::getLastErrorMsg](yaf-application.getlasterrormsg.md)— Отримати останнє повідомлення про помилку
-   [Yaf\_Application::getLastErrorNo](yaf-application.getlasterrorno.md)— Отримати код останньої помилки
-   [Yaf\_Application::getModules](yaf-application.getmodules.md)— Отримати імена заявлених модулів
-   [Yaf\_Application::run](yaf-application.run.md) \- Запустити Yaf\_Application
-   [Yaf\_Application::setAppDirectory](yaf-application.setappdirectory.md)— Змінити директорію програми

Клас YafApplication

-   [« Конфигурация приложения](yaf.appconfig.html)
    
-   [Yaf\_Application::app »](yaf-application.app.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafApplication
    

# Клас YafApplication

(No version information available, might only be in Git)

## Вступ

[Yaf\_Application](class.yaf-application.html) забезпечує ініціалізацію об'єкта для додатків які надають ресурси, що використовуються, загальні та модульні bootstrap-класи та перевірки залежностей.

> **Зауваження**
> 
> [Yaf\_Application](class.yaf-application.html) реалізує шаблоном singleton, та [Yaf\_Application](class.yaf-application.html) не може бути серіалізований або десеріалізований що викликає проблеми, коли ви намагаєтеся використовувати PHPUnit щоб написати деякі тести для Yaf.
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

app

modules

running

environ

## Зміст

-   [Yaf\_Application::app](yaf-application.app.html) — Вийняти екземпляр програми
-   [Yaf\_Application::bootstrap](yaf-application.bootstrap.html) - Викликати bootstrap
-   [Yaf\_Application::clearLastError](yaf-application.clearlasterror.html) — Очищення інформації з останньої помилки
-   [Yaf\_Application::\_\_construct](yaf-application.construct.html) - Конструктор класу YafApplication
-   [Yaf\_Application::\_\_destruct](yaf-application.destruct.html) - Деструктор YafApplication
-   [Yaf\_Application::environ](yaf-application.environ.html) — Отримати значення оточення
-   [Yaf\_Application::execute](yaf-application.execute.html) - Запустити callback-функцію
-   [Yaf\_Application::getAppDirectory](yaf-application.getappdirectory.html) — Отримати директорію програми
-   [Yaf\_Application::getConfig](yaf-application.getconfig.html) — Отримати екземпляр класу конфігурації
-   [Yaf\_Application::getDispatcher](yaf-application.getdispatcher.html) - Отримати екземпляр класу YafDispatcher
-   [Yaf\_Application::getLastErrorMsg](yaf-application.getlasterrormsg.html) — Отримати останнє повідомлення про помилку
-   [Yaf\_Application::getLastErrorNo](yaf-application.getlasterrorno.html) — Отримати код останньої помилки
-   [Yaf\_Application::getModules](yaf-application.getmodules.html) — Отримати імена заявлених модулів
-   [Yaf\_Application::run](yaf-application.run.html) - Запустити YafApplication
-   [Yaf\_Application::setAppDirectory](yaf-application.setappdirectory.html) — Змінити директорію програми
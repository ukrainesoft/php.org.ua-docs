---
navigation:
  - yaf.appconfig.md: « Конфигурация приложения
  - yaf-application.app.html: 'YafApplication::app »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafApplication
---
# Клас YafApplication

(No version information available, might only be in Git)

## Вступ

[YafApplication](class.yaf-application.md) забезпечує ініціалізацію об'єкта для додатків які надають ресурси, що використовуються, загальні та модульні bootstrap-класи та перевірки залежностей.

> **Зауваження**
> 
> [YafApplication](class.yaf-application.html) реалізує шаблоном singleton, та [YafApplication](class.yaf-application.md) не може бути серіалізований або десеріалізований що викликає проблеми, коли ви намагаєтеся використовувати PHPUnit щоб написати деякі тести для Yaf.
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

-   [YafApplication::app](yaf-application.app.md) — Вийняти екземпляр програми
-   [YafApplication::bootstrap](yaf-application.bootstrap.md) - Викликати bootstrap
-   [YafApplication::clearLastError](yaf-application.clearlasterror.md) — Очищення інформації з останньої помилки
-   [YafApplication::construct](yaf-application.construct.md) - Конструктор класу YafApplication
-   [YafApplication::destruct](yaf-application.destruct.md) - Деструктор YafApplication
-   [YafApplication::environ](yaf-application.environ.md) — Отримати значення оточення
-   [YafApplication::execute](yaf-application.execute.md) - Запустити callback-функцію
-   [YafApplication::getAppDirectory](yaf-application.getappdirectory.md) — Отримати директорію програми
-   [YafApplication::getConfig](yaf-application.getconfig.md) — Отримати екземпляр класу конфігурації
-   [YafApplication::getDispatcher](yaf-application.getdispatcher.md) - Отримати екземпляр класу YafDispatcher
-   [YafApplication::getLastErrorMsg](yaf-application.getlasterrormsg.md) — Отримати останнє повідомлення про помилку
-   [YafApplication::getLastErrorNo](yaf-application.getlasterrorno.md) — Отримати код останньої помилки
-   [YafApplication::getModules](yaf-application.getmodules.md) — Отримати імена заявлених модулів
-   [YafApplication::run](yaf-application.run.md) - Запустити YafApplication
-   [YafApplication::setAppDirectory](yaf-application.setappdirectory.md) — Змінити директорію програми

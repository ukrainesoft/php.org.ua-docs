---
navigation:
  - yaf-view-simple.setscriptpath.md: '« YafViewSimple::setScriptPath'
  - yaf-loader.autoload.md: 'YafLoader::autoload »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafLoader
---
# Клас YafLoader

(Yaf >=1.0.0)

## Вступ

**YafLoader** представляє комплексне рішення для автозавантаження Yaf.

При першому вилученні екземпляра [YafApplication](class.yaf-application.md) **YafLoader** створює екземпляр-одиначок і реєструється за допомогою splautoload. Ви отримуєте екземпляр, використовуючи [YafLoader::getInstance()](yaf-loader.getinstance.md)

**YafLoader** спробує завантажити клас лише один раз, у разі виникнення помилки, залежить від [yaf.usesplauload](yaf.configuration.md#ini.yaf.use-spl-autoload)якщо ця конфігурація включена [YafLoader::autoload()](yaf-loader.autoload.md) поверне **`false`**, таким чином надаючи можливість іншої функції автозавантаження. Якщо вимкнено (за замовчуванням), [YafLoader::autoload()](yaf-loader.autoload.md) поверне **`true`**, а також спрацює дуже корисне попередження (корисно з'ясувати, чому клас не може бути завантажений).

> **Зауваження**
> 
> Будь ласка, залиште yaf.usesplautoload вимкненим, якщо в бібліотеці немає власного механізму автозавантаження і його неможливо переписати.

За замовчуванням **YafLoader** припускає, що вся бібліотека (сценарій, визначений класом) зберігається в [каталоге глобальной библиотеки](yaf.configuration.md#ini.yaf.library), який визначено у php.ini (yaf.library).

Якщо ви хочете за допомогою **YafLoader** виконати пошук деяких класів (бібліотек) у [каталог локальних класів](class.yaf-loader.md#yaf-loader.props.library) (який визначений в application.ini, це за замовчуванням [application.directory](yaf.appconfig.md#configuration.yaf.directory). "/library"), ви повинні зареєструвати префікс класу, використовуючи [YafLoader::registerLocalNameSpace()](yaf-loader.registerlocalnamespace.md)

Давайте подивимося кілька прикладів (за умови, що APPLICATIONPATH [application.directory](yaf.appconfig.md#configuration.yaf.directory)

**Приклад #1 Приклад конфігурації**

// Передбачаються такі налаштування в php.ini: yaf.library = "/globaldir"

/ / Передбачаються наступні налаштування в php.ini: application.library = APPLICATIONPATH "/library"

Передбачається, що зареєстровано такий локальний простір імен:

**Приклад #2 Зареєструвати локальний простір імен**

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
     public function _initLoader($dispatcher) {
          Yaf_Loader::getInstance()->registerLocalNameSpace(array("Foo", "Bar"));
     }
?>
```

Тоді приклад автозавантаження:

**Приклад #3 Приклад завантаження класу**

class FooBarTest => // APPLICATIONPATH/library/Foo/Bar/Test.php

class GLOName => ///globaldir/Glo/Name.php

class BarNonTest ///globaldir/Barnon/Test.php

**Приклад #4 Приклад завантаження класу імен**

class FooBarDummy => // APPLICATIONPATH/library/Foo/Bar/Dummy.php

class FooBarBarDummy => ///globaldir/FooBar/Bar/Dummy.php

Ви можете помітити, що всі папки з першою літерою заголовними, ви можете зробити їх малими, встановивши [yaf.lowcasepath](yaf.configuration.md#ini.yaf.lowcase-path) = On у php.ini.

**YafLoader** також призначений для завантаження класів MVC, і правило таке:

**Приклад #5 Приклад завантаження класу MVC**

Controller Classes => // APPLICATIONPATH/controllers/

Model Classes => // APPLICATIONPATH/models/

Plugin Classes => // APPLICATIONPATH/plugins/

Yaf ідентифікує суфікс класу (за умовчанням, ви також можете змінити його на префікс, змінивши конфігурацію [yaf.namesuffix](yaf.configuration.md#ini.yaf.name-suffix)), щоб вирішити, чи є він класом MVC:

**Приклад #6 Класові відмінності MVC**

Controller Classes => // Controller

Model Classes => // Model

Plugin Classes => // Plugin

кілька прикладів:

**Приклад #7 Приклад завантаження MVC**

class IndexController // APPLICATIONPATH/controllers/Index.php

class DataModel => // APPLICATIONPATH/models/Data.php

class DummyPlugin => // APPLICATIONPATH/plugins/Dummy.php

class AУTestModel => // APPLICATIONPATH/models/A/B/Test.php

> **Зауваження**
> 
> Починаючи з 2.1.18, Yaf підтримує автозавантаження контролерів для сторони скрипта користувача (що означає автозавантаження, що запускається користувальницьким скриптом php, наприклад: доступ до статичної властивості контролера в Bootstrap або плагінах). , яка називається "APPLICATIONPATH/controllers/".

також на каталог буде впливати [yaf.lowcasepath](yaf.configuration.md#ini.yaf.lowcase-path)

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Loader
     
     {
    
    /* Свойства */
    
     protected
      $_local_ns;

    protected
      $_library;

    protected
      $_global_library;

    static
      $_instance;



    /* Методы */
    
   private __construct()

    public autoload(): void
public clearLocalNamespace(): void
public static getInstance(): void
public getLibraryPath(bool $is_global = false): Yaf_Loader
public getLocalNamespace(): void
public getNamespacePath(string $namespaces): string
public getNamespaces(): array
public static import(): void
public isLocalName(): void
public registerLocalNamespace(mixed $prefix): void
public registerNamespace(string|array $namespaces, string $path = ?): bool
public setLibraryPath(string $directory, bool $is_global = false): Yaf_Loader

   }
```

## Властивості

localнс

library

За умовчанням це значення дорівнює [application.directory](yaf.appconfig.md#configuration.yaf.directory) . "/library", ви можете змінити це або application.ini(application.library), або викликати [YafLoader::setLibraryPath()](yaf-loader.setlibrarypath.md)

globallibrary

instance

## Зміст

-   [YafLoader::autoload](yaf-loader.autoload.md) - Призначення autoload
-   [YafLoader::clearLocalNamespace](yaf-loader.clearlocalnamespace.md) — Призначення clearLocalNamespace
-   [YafLoader::construct](yaf-loader.construct.md) - Призначення construct
-   [YafLoader::getInstance](yaf-loader.getinstance.md) — Призначення getInstance
-   [YafLoader::getLibraryPath](yaf-loader.getlibrarypath.md) — Отримує шлях до бібліотеки
-   [YafLoader::getLocalNamespace](yaf-loader.getlocalnamespace.md) — Призначення getLocalNamespace
-   [YafLoader::getNamespacePath](yaf-loader.getnamespacepath.md) — Отримує шлях зареєстрованого простору імен
-   [YafLoader::getLocalNamespace](yaf-loader.getnamespaces.md) — Отримує всю інформацію про зареєстровані простори імен
-   [YafLoader::import](yaf-loader.import.md) - Призначення import
-   [YafLoader::isLocalName](yaf-loader.islocalname.md) — Призначення isLocalName
-   [YafLoader::registerLocalNamespace](yaf-loader.registerlocalnamespace.md) - Реєструє префікс локального класу
-   [YafLoader::registerNamespace](yaf-loader.registernamespace.md) — Реєструє простір імен шляхом пошуку
-   [YafLoader::setLibraryPath](yaf-loader.setlibrarypath.md) — Змінює шлях до бібліотеки

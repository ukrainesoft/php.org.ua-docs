---
navigation:
  - yaf-view-simple.setscriptpath.md: '« Yaf\_View\_Simple::setScriptPath'
  - yaf-loader.autoload.md: 'Yaf\_Loader::autoload »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Loader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Loader

(Yaf >=1.0.0)

## Вступ

**Yaf\_Loader**представляет комплексное решение для автозагрузки для Yaf.

При першому вилученні екземпляра [Yaf\_Application](class.yaf-application.md) **Yaf\_Loader** створює екземпляр-одиначок і реєструється за допомогою spl\_autoload. Ви отримуєте екземпляр, використовуючи [Yaf\_Loader::getInstance()](yaf-loader.getinstance.md)

**Yaf\_Loader** спробує завантажити клас лише один раз, у разі виникнення помилки, залежить від [yaf.use\_spl\_auload](yaf.configuration.md#ini.yaf.use-spl-autoload)якщо ця конфігурація включена [Yaf\_Loader::autoload()](yaf-loader.autoload.md) поверне **`false`**, таким чином надаючи можливість іншої функції автозавантаження. Якщо вимкнено (за замовчуванням), [Yaf\_Loader::autoload()](yaf-loader.autoload.md) поверне **`true`**, а також спрацює дуже корисне попередження (корисно з'ясувати, чому клас не може бути завантажений).

> **Зауваження** :
> 
> Будь ласка, залиште yaf.use\_spl\_autoload вимкненим, якщо в бібліотеці немає власного механізму автозавантаження і його неможливо переписати.

По умолчанию**Yaf\_Loader** припускає, що вся бібліотека (сценарій, визначений класом) зберігається в [каталог глобальної бібліотеки](yaf.configuration.md#ini.yaf.library), який визначено у php.ini (yaf.library).

Якщо ви хочете за допомогою **Yaf\_Loader** виконати пошук деяких класів (бібліотек) у [каталог локальних класів](class.yaf-loader.md#yaf-loader.props.library) (який визначений в application.ini, це за замовчуванням [application.directory](yaf.appconfig.md#configuration.yaf.directory). . "/library"), ви повинні зареєструвати префікс класу, використовуючи [Yaf\_Loader::registerLocalNameSpace()](yaf-loader.registerlocalnamespace.md)

Давайте подивимося кілька прикладів (за умови, що APPLICATION\_PATH[application.directory](yaf.appconfig.md#configuration.yaf.directory)):

**Приклад #1 Приклад конфігурації**

// Передбачаються такі налаштування в php.ini: yaf.library = "/global\_dir"

/ / Передбачаються наступні налаштування в php.ini: application.library = APPLICATION\_PATH "/library"

Передбачається, що зареєстровано такий локальний простір імен:

**Приклад #2 Зареєструвати локальний простір імен**

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
     public function _initLoader($dispatcher) {
          Yaf_Loader::getInstance()->registerLocalNameSpace(array("Foo", "Bar"));
     }
?>
```

Тоді приклад автозавантаження:

**Приклад #3 Приклад завантаження класу**

class Foo\_Bar\_Test => // APPLICATION\_PATH/library/Foo/Bar/Test.php

class GLO\_Name => // /global\_dir/Glo/Name.php

class BarNon\_Test // /global\_dir/Barnon/Test.php

**Приклад #4 Приклад завантаження класу імен**

class\\Foo\\Bar\\Dummy => // APPLICATION\_PATH/library/Foo/Bar/Dummy.php

class\\FooBar\\Bar\\Dummy => // /global\_dir/FooBar/Bar/Dummy.php

Ви можете помітити, що всі папки з першою літерою заголовними, ви можете зробити їх малими, встановивши [yaf.lowcase\_path](yaf.configuration.md#ini.yaf.lowcase-path)\= On в php.ini.

**Yaf\_Loader** також призначений для завантаження класів MVC, і правило таке:

**Приклад #5 Приклад завантаження класу MVC**

Controller Classes => // APPLICATION\_PATH/controllers/

Model Classes => // APPLICATION\_PATH/models/

Plugin Classes => // APPLICATION\_PATH/plugins/

Yaf ідентифікує суфікс класу (за умовчанням, ви також можете змінити його на префікс, змінивши конфігурацію [yaf.name\_suffix](yaf.configuration.md#ini.yaf.name-suffix)), щоб вирішити, чи є він класом MVC:

**Приклад #6 Класові відмінності MVC**

Controller Classes => // \*\*\*Controller

Model Classes => // \*\*\*Model

Plugin Classes => // \*\*\*Plugin

кілька прикладів:

**Приклад #7 Приклад завантаження MVC**

class IndexController // APPLICATION\_PATH/controllers/Index.php

class DataModel => // APPLICATION\_PATH/models/Data.php

class DummyPlugin => // APPLICATION\_PATH/plugins/Dummy.php

class A\_B\_TestModel => // APPLICATION\_PATH/models/A/B/Test.php

> **Зауваження** :
> 
> Починаючи з 2.1.18, Yaf підтримує автозавантаження контролерів для сторони скрипта користувача (що означає автозавантаження, що запускається користувальницьким скриптом php, наприклад: доступ до статичної властивості контролера в Bootstrap або плагінах). , яка називається "APPLICATION\_PATH/controllers/".

також на каталог буде впливати [yaf.lowcase\_path](yaf.configuration.md#ini.yaf.lowcase-path)

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

\_local\_ns

\_library

За умовчанням це значення дорівнює [application.directory](yaf.appconfig.md#configuration.yaf.directory) . "/library", ви можете змінити це або application.ini(application.library), або викликати [Yaf\_Loader::setLibraryPath()](yaf-loader.setlibrarypath.md)

\_global\_library

\_instance

## Зміст

-   [Yaf\_Loader::autoload](yaf-loader.autoload.md) \- Призначення autoload
-   [Yaf\_Loader::clearLocalNamespace](yaf-loader.clearlocalnamespace.md)— Призначення clearLocalNamespace
-   [Yaf\_Loader::\_\_construct](yaf-loader.construct.md) \- Призначення\_\_construct
-   [Yaf\_Loader::getInstance](yaf-loader.getinstance.md)— Призначення getInstance
-   [Yaf\_Loader::getLibraryPath](yaf-loader.getlibrarypath.md)— Отримує шлях до бібліотеки
-   [Yaf\_Loader::getLocalNamespace](yaf-loader.getlocalnamespace.md)— Призначення getLocalNamespace
-   [Yaf\_Loader::getNamespacePath](yaf-loader.getnamespacepath.md)— Отримує шлях зареєстрованого простору імен
-   [Yaf\_Loader::getLocalNamespace](yaf-loader.getnamespaces.md)— Отримує всю інформацію про зареєстровані простори імен
-   [Yaf\_Loader::import](yaf-loader.import.md) \- Призначення import
-   [Yaf\_Loader::isLocalName](yaf-loader.islocalname.md)— Призначення isLocalName
-   [Yaf\_Loader::registerLocalNamespace](yaf-loader.registerlocalnamespace.md) \- Реєструє префікс локального класу
-   [Yaf\_Loader::registerNamespace](yaf-loader.registernamespace.md)— Реєструє простір імен шляхом пошуку
-   [Yaf\_Loader::setLibraryPath](yaf-loader.setlibrarypath.md)— Змінює шлях до бібліотеки

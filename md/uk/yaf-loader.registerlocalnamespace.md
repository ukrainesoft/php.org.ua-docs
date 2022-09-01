---
navigation:
  - yaf-loader.islocalname.html: '« YafLoader::isLocalName'
  - yaf-loader.registernamespace.html: 'YafLoader::registerNamespace »'
  - index.md: PHP Manual
  - class.yaf-loader.html: YafLoader
title: 'YafLoader::registerLocalNamespace'
---
# YafLoader::registerLocalNamespace

(Yaf >=1.0.0)

YafLoader::registerLocalNamespace — Реєструє префікс локального класу

### Опис

```methodsynopsis
public Yaf_Loader::registerLocalNamespace(mixed $prefix): void
```

Реєструє префікс локального класу, [YafLoader](class.yaf-loader.html) шукає класи у двох каталогах бібліотеки, один із яких налаштовується за допомогою [application.library.directory](yaf.appconfig.html#configuration.yaf.library) (в application.ini) який називається локальним каталогом бібліотек; інший налаштовується за допомогою [yaf.library](yaf.configuration.html#ini.yaf.library) (в php.ini), який називається глобальним каталогом бібліотеки, оскільки він може використовуватися багатьма програмами на одному сервері.

Коли запускається автозавантаження, [YafLoader](class.yaf-loader.html) визначатиме, у якому каталозі бібліотеки слід шукати, слід шукати, перевіряючи ім'я префікса пропущеного імені класу. Якщо ім'я префікса зареєстроване як localnamespack, шукатиметься в каталозі локальної бібліотеки, інакше — у каталозі глобальної бібліотеки.

> **Зауваження**
> 
> Якщо yaf.library не налаштований, передбачається, що каталог глобальної бібліотеки є каталогом локальної бібліотеки. У цьому випадку всі автозавантаження шукатимуть каталог локальної бібліотеки. Але якщо ви хочете, щоб ваша програма Yaf була стійкою, завжди реєструйте свої власні класи як локальні.

### Список параметрів

`prefix`

Рядок або масив префіксів імені класу. Усі префікси класу з цим префіксом будуть завантажені у шлях локальної бібліотеки.

### Значення, що повертаються

Логічний тип (bool)

### Приклади

**Приклад #1 Приклад використання **YafLoader::registerLocalNamespace()****

```php
<?php
$loader = Yaf_Loader::getInstance('/local/library/', '/global/library');
$loader->registerLocalNamespace("Baidu");
$loader->registerLocalNamespace(array("Sina", "Weibo"));

$loader->autoload("Baidu_Name"); // будет искать в '/local/library/'
$loader->autoload("Sina");       // будет искать в '/local/library/'
$loader->autoload("Global_Name");// будет искать в '/global/library/'
$loader->autoload("Foo_Bar");    // будет искать в '/global/library/'

?>
```

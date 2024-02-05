---
navigation:
  - yaf-application.setappdirectory.md: '« Yaf\_Application::setAppDirectory'
  - class.yaf-dispatcher.md: Yaf\_Dispatcher »
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Bootstrap\_Abstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Bootstrap\_Abstract

(No version information available, might only be in Git)

## Вступ

Bootstrap є механізмом, який використовується для початкового конфігурування чогось до запуску програми.

Користувач може визначити свій власний Bootstrap клас, успадкувавши **Yaf\_Bootstrap\_Abstract**

Будь-який метод, оголошений у класі Bootstrap, що починається на "\_init", буде викликаний [Yaf\_Application::bootstrap()](yaf-application.bootstrap.md) один за одним відповідно до заданої послідовності.

## Приклади

**Приклад #1 Приклад використання Bootstrap**

```php
<?php
   /* класс bootstrap должен быть задан в ./application/Bootstrap.php */
   class Bootstrap extends Yaf_Bootstrap_Abstract {
        public function _initConfig(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
        public function _initPlugin(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
   }

   $config = array(
       "application" => array(
           "directory" => dirname(__FILE__) . "/application/",
       ),
   );

   $app = new Yaf_Application($config);
   $app->bootstrap();
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(22) "Bootstrap::_initConfig"
string(22) "Bootstrap::_initPlugin"
```

## Огляд класів

```classsynopsis


    
    
     
      abstract
      class Yaf_Bootstrap_Abstract
     
     {
    /* Свойства */

    /* Методы */
   }
```

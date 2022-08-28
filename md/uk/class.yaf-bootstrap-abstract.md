Клас YafBootstrapAbstract

-   [« Yaf\_Application::setAppDirectory](yaf-application.setappdirectory.html)
    
-   [Yaf\_Dispatcher »](class.yaf-dispatcher.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafBootstrapAbstract
    

# Клас YafBootstrapAbstract

(No version information available, might only be in Git)

## Вступ

Bootstrap є механізмом, який використовується для початкового конфігурування чогось до запуску програми.

Користувач може визначити свій власний Bootstrap клас, успадкувавши **YafBootstrapAbstract**

Будь-який метод, оголошений у класі Bootstrap, що починається на "init", буде викликаний [Yaf\_Application::bootstrap()](yaf-application.bootstrap.html) один за одним відповідно до заданої послідовності.

## Приклади

**Приклад #1 Приклад використання Bootstrap**

```php
<?php
   /* класс bootstrap должен быть задан в ./application/Bootstrap.php */
   class Bootstrap extends Yaf_Bootstrap_Abstract {
        public function _initConfig(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
        public function _initPlugin(Yaf_Dispatcher $dispatcher) {
            var_dump(__METHOD__);
        }
   }

   $config = array(
       "application" => array(
           "directory" => dirname(__FILE__) . "/application/",
       ),
   );

   $app = new Yaf_Application($config);
   $app->bootstrap();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(22) "Bootstrap::_initConfig"
string(22) "Bootstrap::_initPlugin"
```

## Огляд класів

```synopsis


    
    
     
      abstract
      class Yaf_Bootstrap_Abstract
     
     {
    /* Свойства */

    /* Методы */
   }
```
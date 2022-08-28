Вступ

-   [« WDDX](book.wddx.html)
    
-   [Установка и настройка »](wddx.setup.html)
    
-   [PHP Manual](index.html)
    
-   [WDDX](book.wddx.html)
    
-   Вступ
    

# Вступ

**Увага**

Модуль оголошено *Застарілим* і *ВИДАЛЕНО З ЯДРУ* починаючи з PHP 7.4.0.

Ці функції призначені для роботи з [» WDDX](http://www.openwddx.org/)

**Увага**

Не передавайте недовірені дані користувача в [wddx\_deserialize()](function.wddx-deserialize.html). Десеріалізація може призвести до завантаження та запуску шкідливого коду під час інстанціювання та автозавантаження об'єкта. Використовуйте безпечний стандартний формат передачі інформації, такий як JSON (за допомогою [json\_decode()](function.json-decode.html) і [json\_encode()](function.json-encode.html)
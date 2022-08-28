Правила

-   [« Глобальное пространство имён](userlandnaming.globalnamespace.html)
    
-   [Советы »](userlandnaming.tips.html)
    
-   [PHP Manual](index.html)
    
-   [Руководство по именованию](userlandnaming.html)
    
-   Правила
    

## Правила

Наступний список правил дає огляд прав іменування, які PHP залишає собі при виборі нових ідентифікаторів. Повним керівництвом є офіційний[» Стандарт написания кода](https://github.com/php/php-src/raw/master/CODING_STANDARDS.md)":

-   PHP має глобальний простір імен, але намагається знаходити хороші описові імена і уникати будь-яких очевидних колізій.
    
-   Імена функцій використовують підкреслення між словами, а імена класів використовують як `camelCase`, так і `PascalCase`
    
-   PHP додає префікс до глобальних імен, що належать до модуля з ім'ям цього модуля. У минулому було безліч винятків із цього правила, наприклад:
    
    -   [curl\_close()](function.curl-close.html)
        
    -   [mysql\_query()](function.mysql-query.html)
        
    -   PREGSPLITДІЛИМОCAPTURE
        
    -   new DOMDocument()
        
    -   [strpos()](function.strpos.html) (Приклад виключення, допущеного в минулому)
        
    -   new SplFileObject()
        
-   Тим не менш, ітератори та винятки просто отримують постфікси.`Iterator`"і"`Exception`". Приклади:
    
    -   [ArrayIterator](class.arrayiterator.html)
        
    -   [LogicException](class.logicexception.html)
        
-   PHP резервує всі ідентифікатори, що починаються з `__` як магічні. Рекомендується не створювати ідентифікатори, що починаються з `__`крім як з метою використовувати документовану магічну функціональність. Приклади:
    
    -   [\_\_get()](language.oop5.overloading.html#object.get)
        
    -   [\_\_autoload()](function.autoload.html)
---
navigation:
  - userlandnaming.globalnamespace.md: « Глобальний простір імен
  - userlandnaming.tips.md: Поради »
  - index.md: PHP Manual
  - userlandnaming.md: Посібник з іменування
title: Правила
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Правила

Наступний список правил дає огляд прав іменування, які PHP залишає собі при виборі нових ідентифікаторів. Повним керівництвом є офіційний[» Стандарт написання коду](https://github.com/php/php-src/raw/master/CODING_STANDARDS.md)":

-   PHP має глобальний простір імен, але намагається знаходити хороші описові імена і уникати будь-яких очевидних колізій.
    
-   Імена функцій використовують підкреслення між словами, а імена класів використовують як`camelCase`, так и`PascalCase`
    
-   PHP додає префікс до глобальних імен, що належать до модуля з ім'ям цього модуля. У минулому було безліч винятків із цього правила, наприклад:
    
    -   [curl\_close()](function.curl-close.md)
        
    -   [mysql\_query()](function.mysql-query.md)
        
    -   PREG\_SPLIT\_DELIM\_CAPTURE
        
    -   new DOMDocument()
        
    -   [strpos()](function.strpos.md)(Приклад виключення, допущеного в минулому)
        
    -   new SplFileObject()
        
-   Тим не менш, ітератори та винятки просто отримують постфікси.`Iterator`"і"`Exception`". Приклади:
    
    -   [ArrayIterator](class.arrayiterator.md)
        
    -   [LogicException](class.logicexception.md)
        
-   PHP резервує всі ідентифікатори, що починаються з`__`як магічні. Рекомендується не створювати ідентифікатори, що починаються з`__`крім як з метою використовувати документовану магічну функціональність. Приклади:
    
    -   [\_\_get()](language.oop5.overloading.md#object.get)
        
    -   [\_\_autoload()](function.autoload.md)

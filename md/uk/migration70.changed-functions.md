Змінені функції

-   [« Функціональність, оголошена застарілою в PHP 7.0.x](migration70.deprecated.html)
    
-   [Нові функції »](migration70.new-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.html)
    
-   Змінені функції
    

## Змінені функції

### Ядро PHP

-   [debugzvaldump()](function.debug-zval-dump.html) тепер друкує "int" замість "long", і "float" замість "double"
-   [dirname()](function.dirname.html) приймає другий, необов'язковий параметр `depth`, для отримання імені директорії на `depth` рівнів вище за поточну.
-   [getrusage()](function.getrusage.html) тепер підтримується у Windows.
-   Функції [mktime()](function.mktime.html) і [gmmktime()](function.gmmktime.html) більше не приймають параметр `is_dst`
-   Функція [pregreplace()](function.preg-replace.html) більше не підтримує "e" (**`PREG_REPLACE_EVAL`**). Натомість використовуйте [pregreplacecallback()](function.preg-replace-callback.html)
-   Функція [setlocale()](function.setlocale.html) більше не приймає параметр `category` переданий у вигляді рядка. Тепер потрібно використовувати константи **`LC_*`**
-   Функції [exec()](function.exec.html) [system()](function.system.html) і [passthru()](function.passthru.html) тепер захищено від NULL-байта.
-   [shmopopen()](function.shmop-open.html) тепер повертає не ціле, а ресурс, який має бути переданий у [shmopsize()](function.shmop-size.html) [shmopwrite()](function.shmop-write.html) [shmopread()](function.shmop-read.html) [shmopclose()](function.shmop-close.html) і [shmopdelete()](function.shmop-delete.html)
-   [substr()](function.substr.html) і [iconvsubstr()](function.iconv-substr.html) повертають порожній рядок, якщо start дорівнює довжині рядка.
-   Використання [xmlparserfree()](function.xml-parser-free.html) тепер недостатньо для звільнення ресурсу парсера, якщо він посилається на об'єкт, а цей об'єкт посилається ресурс парсера. У такому випадку необхідно додатково видалити вручну (unset) змінну $parser.
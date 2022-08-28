Змінені функції

-   [« Функциональность, объявленная устаревшей в PHP 7.0.x](migration70.deprecated.html)
    
-   [Новые функции »](migration70.new-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.html)
    
-   Змінені функції
    

## Змінені функції

### Ядро PHP

-   [debug\_zval\_dump()](function.debug-zval-dump.html) тепер друкує "int" замість "long", і "float" замість "double"
-   [dirname()](function.dirname.html) приймає другий, необов'язковий параметр `depth`, для отримання імені директорії на `depth` рівнів вище за поточну.
-   [getrusage()](function.getrusage.html) тепер підтримується у Windows.
-   Функції [mktime()](function.mktime.html) і [gmmktime()](function.gmmktime.html) більше не приймають параметр `is_dst`
-   Функція [preg\_replace()](function.preg-replace.html) більше не підтримує "e" (**`PREG_REPLACE_EVAL`**). Натомість використовуйте [preg\_replace\_callback()](function.preg-replace-callback.html)
-   Функція [setlocale()](function.setlocale.html) більше не приймає параметр `category` переданий у вигляді рядка. Тепер потрібно використовувати константи **`LC_*`**
-   Функції [exec()](function.exec.html) [system()](function.system.html) і [passthru()](function.passthru.html) тепер захищено від NULL-байта.
-   [shmop\_open()](function.shmop-open.html) тепер повертає не ціле, а ресурс, який має бути переданий у [shmop\_size()](function.shmop-size.html) [shmop\_write()](function.shmop-write.html) [shmop\_read()](function.shmop-read.html) [shmop\_close()](function.shmop-close.html) і [shmop\_delete()](function.shmop-delete.html)
-   [substr()](function.substr.html) і [iconv\_substr()](function.iconv-substr.html) повертають порожній рядок, якщо start дорівнює довжині рядка.
-   Використання [xml\_parser\_free()](function.xml-parser-free.html) тепер недостатньо для звільнення ресурсу парсера, якщо він посилається на об'єкт, а цей об'єкт посилається ресурс парсера. У такому випадку необхідно додатково видалити вручну (unset) змінну $parser.
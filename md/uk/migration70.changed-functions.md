---
navigation:
  - migration70.deprecated.md: '« Функціональність, оголошена застарілою в PHP 7.0.x'
  - migration70.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration70.md: Миграция с PHP 5.6.x на PHP 7.0.x
title: Змінені функції
---
## Змінені функції

### Ядро PHP

-   [debugzvaldump()](function.debug-zval-dump.md) тепер друкує "int" замість "long", і "float" замість "double"
-   [dirname()](function.dirname.md) приймає другий, необов'язковий параметр `depth`, для отримання імені директорії на `depth` рівнів вище за поточну.
-   [getrusage()](function.getrusage.md) тепер підтримується у Windows.
-   Функції [mktime()](function.mktime.md) і [gmmktime()](function.gmmktime.md) більше не приймають параметр `is_dst`
-   Функція [pregreplace()](function.preg-replace.md) більше не підтримує "e" (**`PREG_REPLACE_EVAL`**). Натомість використовуйте [pregreplacecallback()](function.preg-replace-callback.md)
-   Функція [setlocale()](function.setlocale.md) більше не приймає параметр `category` переданий у вигляді рядка. Тепер потрібно використовувати константи **`LC_*`**
-   Функції [exec()](function.exec.md) [system()](function.system.md) і [passthru()](function.passthru.md) тепер захищено від NULL-байта.
-   [shmopopen()](function.shmop-open.md) тепер повертає не ціле, а ресурс, який має бути переданий у [shmopsize()](function.shmop-size.md) [shmopwrite()](function.shmop-write.md) [shmopread()](function.shmop-read.md) [shmopclose()](function.shmop-close.md) і [shmopdelete()](function.shmop-delete.md)
-   [substr()](function.substr.md) і [iconvsubstr()](function.iconv-substr.md) повертають порожній рядок, якщо start дорівнює довжині рядка.
-   Використання [xmlparserfree()](function.xml-parser-free.md) тепер недостатньо для звільнення ресурсу парсера, якщо він посилається на об'єкт, а цей об'єкт посилається ресурс парсера. У такому випадку необхідно додатково видалити вручну (unset) змінну $parser.

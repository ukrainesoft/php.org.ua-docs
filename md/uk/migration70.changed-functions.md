---
navigation:
  - migration70.deprecated.md: '« Функціональність, оголошена застарілою в PHP 7.0.x'
  - migration70.new-functions.md: Нові функції »
  - index.md: PHP Manual
  - migration70.md: Міграція з PHP 5.6.x на PHP 7.0.x
title: Змінені функції
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Змінені функції

### Ядро PHP

-   [debug\_zval\_dump()](function.debug-zval-dump.md) тепер друкує "int" замість "long", і "float" замість "double"
-   [dirname()](function.dirname.md)приймає другий, необов'язковий параметр`depth`, для отримання імені директорії на`depth`рівнів вище за поточну.
-   [getrusage()](function.getrusage.md) тепер підтримується у Windows.
-   Функції [mktime()](function.mktime.md) і [gmmktime()](function.gmmktime.md)більше не приймають параметр`is_dst`
-   Функция[preg\_replace()](function.preg-replace.md) більше не підтримує "\\e" (**`PREG_REPLACE_EVAL`**). Натомість використовуйте[preg\_replace\_callback()](function.preg-replace-callback.md)
-   Функция[setlocale()](function.setlocale.md)більше не приймає параметр`category`переданий у вигляді рядка. Тепер потрібно використовувати константи\*\*`LC_*`\*\*
-   Функції [exec()](function.exec.md) [system()](function.system.md) і [passthru()](function.passthru.md)тепер захищено від NULL-байта.
-   [shmop\_open()](function.shmop-open.md)тепер повертає не ціле, а ресурс, який має бути переданий у[shmop\_size()](function.shmop-size.md) [shmop\_write()](function.shmop-write.md) [shmop\_read()](function.shmop-read.md) [shmop\_close()](function.shmop-close.md) і [shmop\_delete()](function.shmop-delete.md)
-   [substr()](function.substr.md) і [iconv\_substr()](function.iconv-substr.md)повертають порожній рядок, якщо start дорівнює довжині рядка.
-   Использование[xml\_parser\_free()](function.xml-parser-free.md)тепер недостатньо для звільнення ресурсу парсера, якщо він посилається на об'єкт, а цей об'єкт посилається на ресурс парсеру. У такому випадку необхідно додатково видалити вручну (unset) змінну $parser.

---
navigation:
  - mbstring.supported-encodings.md: « Підтримувані кодування символів
  - mbstring.php4.req.md: Вимоги до кодування символів у PHP »
  - index.md: PHP Manual
  - book.mbstring.md: Багатобайтові рядки
title: Механізм навантаження функцій
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Механізм навантаження функцій

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Найчастіше змусити працювати існуючий PHP-додаток у багатобайтовому оточенні виявляється досить важким завданням. Це відбувається тому, що більшість PHP-додатків написано з використанням стандартних функцій обробки рядків, таких як [substr()](function.substr.md), які не вміють працювати з рядками у багатобайтових кодуваннях

mbstring підтримує механізм 'перевантаження функцій', який дозволяє повідомити додаток про те, що використовується багатобайтове кодування без модифікації коду, що відповідає за роботу з рядками. Наприклад, якщо увімкнено навантаження функцій, то функція [mb\_substr()](function.mb-substr.md) буде викликатися замість [substr()](function.substr.md). Цей механізм у багатьох випадках дозволяє портувати додатки, що підтримують тільки однобайтові кодування, багатобайтне оточення.

Для використання механізму перевантаження функцій потрібно встановити налаштування `mbstring.func_overload` у php.ini позитивне значення, яке є комбінацією бітових масок, що визначають категорії функцій, які потрібно перевантажувати. Це буде число 1 для навантаження функції [mail()](function.mail.md). 2 для рядкових функцій; 4 для функцій регулярних виразів. Наприклад, якщо значення налаштування дорівнює 7, то поштові, рядкові та функції регулярних виразів перевантажуватимуться. Список перевантажуваних функцій наведено нижче.

**Функції, які будуть перевантажені**

| значение настройки mbstring.func\_overload | исходная функция | перегруженная функция |
| --- | --- | --- |
|  | [mail()](function.mail.md) | [mb\_send\_mail()](function.mb-send-mail.md) |
|  | [strlen()](function.strlen.md) | [mb\_strlen()](function.mb-strlen.md) |
|  | [strpos()](function.strpos.md) | [mb\_strpos()](function.mb-strpos.md) |
|  | [strrpos()](function.strrpos.md) | [mb\_strrpos()](function.mb-strrpos.md) |
|  | [substr()](function.substr.md) | [mb\_substr()](function.mb-substr.md) |
|  | [strtolower()](function.strtolower.md) | [mb\_strtolower()](function.mb-strtolower.md) |
|  | [strtoupper()](function.strtoupper.md) | [mb\_strtoupper()](function.mb-strtoupper.md) |
|  | [stripos()](function.stripos.md) | [mb\_stripos()](function.mb-stripos.md) |
|  | [strripos()](function.strripos.md) | [mb\_strripos()](function.mb-strripos.md) |
|  | [strstr()](function.strstr.md) | [mb\_strstr()](function.mb-strstr.md) |
|  | [stristr()](function.stristr.md) | [mb\_stristr()](function.mb-stristr.md) |
|  | [strrchr()](function.strrchr.md) | [mb\_strrchr()](function.mb-strrchr.md) |
|  | [substr\_count()](function.substr-count.md) | [mb\_substr\_count()](function.mb-substr-count.md) |

> **Зауваження** :
> 
> Не рекомендується використовувати навантаження функцій у контексті кожної директорії, оскільки домогтися стабільної роботи в цьому випадку поки не вдалося, і це може призвести до несподіваної поведінки програми.

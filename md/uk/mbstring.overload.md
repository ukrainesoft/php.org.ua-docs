---
navigation:
  - mbstring.supported-encodings.html: « Підтримувані кодування символів
  - mbstring.php4.req.md: Вимоги до кодування символів у PHP »
  - index.md: PHP Manual
  - book.mbstring.md: Багатобайтові рядки
title: Механізм навантаження функцій
---
# Механізм навантаження функцій

**Увага**

Ця функціональність оголошена *застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Найчастіше змусити працювати існуючий PHP-додаток у багатобайтовому оточенні виявляється досить важким завданням. Це відбувається тому, що більшість PHP-додатків написано з використанням стандартних функцій обробки рядків, таких як [substr()](function.substr.md), які не вміють працювати з рядками у багатобайтових кодуваннях

mbstring підтримує механізм 'перевантаження функцій', який дозволяє повідомити додаток про те, що використовується багатобайтове кодування без модифікації коду, що відповідає за роботу з рядками. Наприклад, якщо увімкнено навантаження функцій, то функція [мбsubstr()](function.mb-substr.md) буде викликатися замість [substr()](function.substr.md). Цей механізм у багатьох випадках дозволяє портувати додатки, що підтримують лише однобайтові кодування, багатобайтне оточення.

Для використання механізму перевантаження функцій потрібно встановити налаштування `mbstring.func_overload` у php.ini позитивне значення, яке є комбінацією бітових масок, що визначають категорії функцій, які потрібно перевантажувати. Це буде число 1 для навантаження функції [mail()](function.mail.md). 2 для рядкових функцій; 4 для функцій регулярних виразів. Наприклад, якщо значення налаштування дорівнює 7, то поштові, рядкові та функції регулярних виразів перевантажуватимуться. Список перевантажуваних функцій наведено нижче.

**Функції, які будуть перевантажені**

| значение настройки mbstring.func\_overload | исходная функция | перегруженная функция |
| --- | --- | --- |
|  | [mail()](function.mail.md) | [мбsendmail()](function.mb-send-mail.md) |
|  | [strlen()](function.strlen.md) | [мбstrlen()](function.mb-strlen.md) |
|  | [strpos()](function.strpos.md) | [мбstrpos()](function.mb-strpos.md) |
|  | [strrpos()](function.strrpos.md) | [мбstrrpos()](function.mb-strrpos.md) |
|  | [substr()](function.substr.md) | [мбsubstr()](function.mb-substr.md) |
|  | [strtolower()](function.strtolower.md) | [мбstrtolower()](function.mb-strtolower.md) |
|  | [strtoupper()](function.strtoupper.md) | [мбstrtoupper()](function.mb-strtoupper.md) |
|  | [stripos()](function.stripos.md) | [мбstripos()](function.mb-stripos.md) |
|  | [strripos()](function.strripos.md) | [мбstrripos()](function.mb-strripos.md) |
|  | [strstr()](function.strstr.md) | [мбstrstr()](function.mb-strstr.md) |
|  | [stristr()](function.stristr.md) | [мбstristr()](function.mb-stristr.md) |
|  | [strrchr()](function.strrchr.md) | [мбstrrchr()](function.mb-strrchr.md) |
|  | [substrcount()](function.substr-count.html) | [мбsubstrcount()](function.mb-substr-count.md) |

> **Зауваження**
> 
> Не рекомендується використовувати навантаження функцій у контексті кожної директорії, оскільки домогтися стабільної роботи в цьому випадку поки не вдалося, і це може призвести до несподіваної поведінки програми.

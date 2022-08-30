Механізм навантаження функцій

-   [« Підтримувані кодування символів](mbstring.supported-encodings.html)
    
-   [Вимоги до кодування символів у PHP »](mbstring.php4.req.html)
    
-   [PHP Manual](index.html)
    
-   [Багатобайтові рядки](book.mbstring.html)
    
-   Механізм навантаження функцій
    

# Механізм навантаження функцій

**Увага**

Ця функціональність оголошена *застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Найчастіше змусити працювати існуючий PHP-додаток у багатобайтовому оточенні виявляється досить важким завданням. Це відбувається тому, що більшість PHP-додатків написано з використанням стандартних функцій обробки рядків, таких як [substr()](function.substr.html), які не вміють працювати з рядками у багатобайтових кодуваннях

mbstring підтримує механізм 'перевантаження функцій', який дозволяє повідомити додаток про те, що використовується багатобайтове кодування без модифікації коду, що відповідає за роботу з рядками. Наприклад, якщо увімкнено навантаження функцій, то функція [мбsubstr()](function.mb-substr.html) буде викликатися замість [substr()](function.substr.html). Цей механізм у багатьох випадках дозволяє портувати додатки, що підтримують лише однобайтові кодування, багатобайтне оточення.

Для використання механізму перевантаження функцій потрібно встановити налаштування `mbstring.func_overload` у php.ini позитивне значення, яке є комбінацією бітових масок, що визначають категорії функцій, які потрібно перевантажувати. Це буде число 1 для навантаження функції [mail()](function.mail.html). 2 для рядкових функцій; 4 для функцій регулярних виразів. Наприклад, якщо значення налаштування дорівнює 7, то поштові, рядкові та функції регулярних виразів перевантажуватимуться. Список перевантажуваних функцій наведено нижче.

**Функції, які будуть перевантажені**

| значение настройки mbstring.func\_overload | исходная функция                            | перегруженная функция                            |
|--------------------------------------------|---------------------------------------------|--------------------------------------------------|
|                                            | [mail()](function.mail.html)                | [мбsendmail()](function.mb-send-mail.html)       |
|                                            | [strlen()](function.strlen.html)            | [мбstrlen()](function.mb-strlen.html)            |
|                                            | [strpos()](function.strpos.html)            | [мбstrpos()](function.mb-strpos.html)            |
|                                            | [strrpos()](function.strrpos.html)          | [мбstrrpos()](function.mb-strrpos.html)          |
|                                            | [substr()](function.substr.html)            | [мбsubstr()](function.mb-substr.html)            |
|                                            | [strtolower()](function.strtolower.html)    | [мбstrtolower()](function.mb-strtolower.html)    |
|                                            | [strtoupper()](function.strtoupper.html)    | [мбstrtoupper()](function.mb-strtoupper.html)    |
|                                            | [stripos()](function.stripos.html)          | [мбstripos()](function.mb-stripos.html)          |
|                                            | [strripos()](function.strripos.html)        | [мбstrripos()](function.mb-strripos.html)        |
|                                            | [strstr()](function.strstr.html)            | [мбstrstr()](function.mb-strstr.html)            |
|                                            | [stristr()](function.stristr.html)          | [мбstristr()](function.mb-stristr.html)          |
|                                            | [strrchr()](function.strrchr.html)          | [мбstrrchr()](function.mb-strrchr.html)          |
|                                            | [substrcount()](function.substr-count.html) | [мбsubstrcount()](function.mb-substr-count.html) |

> **Зауваження**
> 
> Не рекомендується використовувати навантаження функцій у контексті кожної директорії, оскільки домогтися стабільної роботи в цьому випадку поки не вдалося, і це може призвести до несподіваної поведінки програми.
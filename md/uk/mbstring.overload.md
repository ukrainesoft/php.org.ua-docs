Механізм навантаження функцій

-   [« Підтримувані кодування символів](mbstring.supported-encodings.html)
    
-   [Вимоги до кодування символів у PHP »](mbstring.php4.req.md)
    
-   [PHP Manual](index.md)
    
-   [Багатобайтові рядки](book.mbstring.md)
    
-   Механізм навантаження функцій
    

# Механізм навантаження функцій

**Увага**

Ця функціональність оголошена *застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Найчастіше змусити працювати існуючий PHP-додаток у багатобайтовому оточенні виявляється досить важким завданням. Це відбувається тому, що більшість PHP-додатків написано з використанням стандартних функцій обробки рядків, таких як [substr()](function.substr.md), які не вміють працювати з рядками у багатобайтових кодуваннях

mbstring підтримує механізм 'перевантаження функцій', який дозволяє повідомити додаток про те, що використовується багатобайтове кодування без модифікації коду, що відповідає за роботу з рядками. Наприклад, якщо увімкнено навантаження функцій, то функція [мбsubstr()](function.mb-substr.html) буде викликатися замість [substr()](function.substr.md). Цей механізм у багатьох випадках дозволяє портувати додатки, що підтримують лише однобайтові кодування, багатобайтне оточення.

Для використання механізму перевантаження функцій потрібно встановити налаштування `mbstring.func_overload` у php.ini позитивне значення, яке є комбінацією бітових масок, що визначають категорії функцій, які потрібно перевантажувати. Це буде число 1 для навантаження функції [mail()](function.mail.md). 2 для рядкових функцій; 4 для функцій регулярних виразів. Наприклад, якщо значення налаштування дорівнює 7, то поштові, рядкові та функції регулярних виразів перевантажуватимуться. Список перевантажуваних функцій наведено нижче.

**Функції, які будуть перевантажені**

| значение настройки mbstring.func\_overload | исходная функция                            | перегруженная функция                            |
|--------------------------------------------|---------------------------------------------|--------------------------------------------------|
|                                            | [mail()](function.mail.md)                  | [мбsendmail()](function.mb-send-mail.html)       |
|                                            | [strlen()](function.strlen.md)              | [мбstrlen()](function.mb-strlen.html)            |
|                                            | [strpos()](function.strpos.md)              | [мбstrpos()](function.mb-strpos.html)            |
|                                            | [strrpos()](function.strrpos.md)            | [мбstrrpos()](function.mb-strrpos.html)          |
|                                            | [substr()](function.substr.md)              | [мбsubstr()](function.mb-substr.html)            |
|                                            | [strtolower()](function.strtolower.md)      | [мбstrtolower()](function.mb-strtolower.html)    |
|                                            | [strtoupper()](function.strtoupper.md)      | [мбstrtoupper()](function.mb-strtoupper.html)    |
|                                            | [stripos()](function.stripos.md)            | [мбstripos()](function.mb-stripos.html)          |
|                                            | [strripos()](function.strripos.md)          | [мбstrripos()](function.mb-strripos.html)        |
|                                            | [strstr()](function.strstr.md)              | [мбstrstr()](function.mb-strstr.html)            |
|                                            | [stristr()](function.stristr.md)            | [мбstristr()](function.mb-stristr.html)          |
|                                            | [strrchr()](function.strrchr.md)            | [мбstrrchr()](function.mb-strrchr.html)          |
|                                            | [substrcount()](function.substr-count.html) | [мбsubstrcount()](function.mb-substr-count.html) |

> **Зауваження**
> 
> Не рекомендується використовувати навантаження функцій у контексті кожної директорії, оскільки домогтися стабільної роботи в цьому випадку поки не вдалося, і це може призвести до несподіваної поведінки програми.
Функції для роботи з багатобайтовими рядками

-   [« Требования, предъявляемые к кодировкам символов в PHP](mbstring.php4.req.html)
    
-   [mb\_check\_encoding »](function.mb-check-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Многобайтовые строки](book.mbstring.html)
    
-   Функції для роботи з багатобайтовими рядками
    

# Функції для роботи з багатобайтовими рядками

# Посилання

Схеми багатобайтного кодування символів та його реалізації досить складні, та його опис перебуває поза цієї документации. Більш вичерпну інформацію про кодування та їх пристрій можна отримати з наведених нижче джерел.

-   Матеріали по Юнікоду
    
    [» http://www.unicode.org/](http://www.unicode.org/)
    
-   Інформація про символи японського/корейського/китайського кодувань
    
    [» https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf](https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf)
    

## Зміст

-   [mb\_check\_encoding](function.mb-check-encoding.html) — Перевіряє, що кодування рядків вибрано правильно
-   [mb\_chr](function.mb-chr.html) — Повертає символ за значенням кодової точки Unicode
-   [mb\_convert\_case](function.mb-convert-case.html) — Здійснює зміну регістру символів у рядку
-   [mb\_convert\_encoding](function.mb-convert-encoding.html) — Перетворює рядок з одного кодування символів на інший
-   [mb\_convert\_kana](function.mb-convert-kana.html) - Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)
-   [mb\_convert\_variables](function.mb-convert-variables.html) — Перетворює символи на змінну з одного кодування на інше
-   [mb\_decode\_mimeheader](function.mb-decode-mimeheader.html) — Декодує рядок у MIME-заголовку
-   [mb\_decode\_numericentity](function.mb-decode-numericentity.html) — Декодує посилання на числовий рядок HTML на символ
-   [mb\_detect\_encoding](function.mb-detect-encoding.html) — Визначення кодування символів
-   [mb\_detect\_order](function.mb-detect-order.html) — Встановлення/отримання списку кодувань для механізмів визначення кодування
-   [mb\_encode\_mimeheader](function.mb-encode-mimeheader.html) — Кодує рядок для MIME-заголовка
-   [mb\_encode\_numericentity](function.mb-encode-numericentity.html) — Кодує символ у числове HTML-посилання
-   [mb\_encoding\_aliases](function.mb-encoding-aliases.html) — Отримує псевдоніми відомого типу кодування
-   [mb\_ereg\_match](function.mb-ereg-match.html) — Збіг з регулярним виразом для багатобайтового рядка
-   [mb\_ereg\_replace\_callback](function.mb-ereg-replace-callback.html) — Виконує пошук та заміну за регулярним виразом за допомогою багатобайтових кодувань використовуючи callback-функцію
-   [mb\_ereg\_replace](function.mb-ereg-replace.html) — Здійснює заміну за регулярним виразом за допомогою багатобайтових кодувань.
-   [mb\_ereg\_search\_getpos](function.mb-ereg-search-getpos.html) — Повертає початкову позицію наступного збігу з регулярним виразом
-   [mb\_ereg\_search\_getregs](function.mb-ereg-search-getregs.html) — Виводить результат останнього порівняння з регулярним виразом
-   [mb\_ereg\_search\_init](function.mb-ereg-search-init.html) — Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного вираження
-   [mb\_ereg\_search\_pos](function.mb-ereg-search-pos.html) — Повертає позицію і довжину ділянки багатобайтового рядка, що збіглася з регулярним виразом.
-   [mb\_ereg\_search\_regs](function.mb-ereg-search-regs.html) — Повертає частину рядка, що збіглася з регулярним виразом.
-   [mb\_ereg\_search\_setpos](function.mb-ereg-search-setpos.html) — Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу
-   [mb\_ereg\_search](function.mb-ereg-search.html) — Пошук відповідності регулярному виразу для рядків у багатобайтових кодуваннях
-   [mb\_ereg](function.mb-ereg.html) — Збіг з регулярним виразом із підтримкою багатобайтових кодувань
-   [mb\_eregi\_replace](function.mb-eregi-replace.html) — Здійснює заміну за регулярним виразом за допомогою багатобайтових символів без урахування регістру
-   [mb\_eregi](function.mb-eregi.html) — Пошук відповідності регулярному виразу за допомогою багатобайтових символів без урахування регістру
-   [mb\_get\_info](function.mb-get-info.html) — Отримує внутрішні налаштування mbstring
-   [mb\_http\_input](function.mb-http-input.html) — Визначення кодування символів вхідних даних HTTP-запиту
-   [mb\_http\_output](function.mb-http-output.html) — Встановлення/отримання кодування символів виводу HTTP
-   [mb\_internal\_encoding](function.mb-internal-encoding.html) — Встановлення/отримання внутрішнього кодування скрипту
-   [mb\_language](function.mb-language.html) — Встановлює/отримує поточну мову
-   [mb\_list\_encodings](function.mb-list-encodings.html) — Повертає масив усіх кодувань, що підтримуються.
-   [mb\_ord](function.mb-ord.html) — Отримує кодову точку символу Unicode
-   [mb\_output\_handler](function.mb-output-handler.html) - Callback-функція, що перетворює кодування символів у вихідному буфері
-   [mb\_parse\_str](function.mb-parse-str.html) — Розбір даних запитів GET/POST/COOKIE та встановлення значень глобальних змінних
-   [mb\_preferred\_mime\_name](function.mb-preferred-mime-name.html) — Отримання набору символів MIME
-   [mb\_regex\_encoding](function.mb-regex-encoding.html) — Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [mb\_regex\_set\_options](function.mb-regex-set-options.html) — Встановлення/отримання стандартних значень для налаштування функцій mbregex
-   [mb\_scrub](function.mb-scrub.html) - Опис
-   [mb\_send\_mail](function.mb-send-mail.html) — Надсилання закодованого повідомлення
-   [mb\_split](function.mb-split.html) — Поділ рядків у багатобайтних кодуваннях, використовуючи регулярний вираз
-   [mb\_str\_split](function.mb-str-split.html) — Якщо заданий багатобайтовий рядок повертає масив символів
-   [mb\_strcut](function.mb-strcut.html) — Отримання частини рядка
-   [mb\_strimwidth](function.mb-strimwidth.html) — Отримання рядка, обрізаного до заданого розміру
-   [mb\_stripos](function.mb-stripos.html) — Реєстронезалежний пошук позиції першого входження одного рядка в інший
-   [mb\_stristr](function.mb-stristr.html) — Знаходить перше входження підрядки у рядку без урахування регістру
-   [mb\_strlen](function.mb-strlen.html) — Отримує довжину рядка
-   [mb\_strpos](function.mb-strpos.html) — Пошук позиції першого входження одного рядка до іншого
-   [mb\_strrchr](function.mb-strrchr.html) — Пошук останнього входження одного рядка до іншого
-   [mb\_strrichr](function.mb-strrichr.html) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [mb\_strripos](function.mb-strripos.html) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [mb\_strrpos](function.mb-strrpos.html) — Пошук позиції останнього входження одного рядка до іншого
-   [mb\_strstr](function.mb-strstr.html) — Знаходить перше входження підрядка у рядку
-   [mb\_strtolower](function.mb-strtolower.html) — Приведення рядка до нижнього регістру
-   [mb\_strtoupper](function.mb-strtoupper.html) — Приведення рядка до верхнього регістру
-   [mb\_strwidth](function.mb-strwidth.html) — Повертає ширину рядка
-   [mb\_substitute\_character](function.mb-substitute-character.html) — Встановити/отримати символ заміни
-   [mb\_substr\_count](function.mb-substr-count.html) — Повертає кількість входжень підрядка
-   [mb\_substr](function.mb-substr.html) — Повертає частину рядка
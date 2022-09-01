---
navigation:
  - mbstring.php4.req.md: « Вимоги до кодування символів у PHP
  - function.mb-check-encoding.html: мбcheckencoding »
  - index.md: PHP Manual
  - book.mbstring.md: Багатобайтові рядки
title: Функції для роботи з багатобайтовими рядками
---
# Функції для роботи з багатобайтовими рядками

# Посилання

Схеми багатобайтного кодування символів та його реалізації досить складні, та його опис перебуває поза цієї документации. Більш вичерпну інформацію про кодування та їх пристрій можна отримати з наведених нижче джерел.

-   Матеріали по Юнікоду
    
    [» http://www.unicode.org/](http://www.unicode.org/)
    
-   Інформація про символи японського/корейського/китайського кодувань
    
    [» https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf](https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf)
    

## Зміст

-   [мбcheckencoding](function.mb-check-encoding.html) — Перевіряє, що кодування рядків вибрано правильно
-   [мбchr](function.mb-chr.html) — Повертає символ за значенням кодової точки Unicode
-   [мбconvertcase](function.mb-convert-case.html) — Здійснює зміну регістру символів у рядку
-   [мбconvertencoding](function.mb-convert-encoding.html) — Перетворює рядок з одного кодування символів на інший
-   [мбconvertkana](function.mb-convert-kana.html) - Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)
-   [мбconvertvariables](function.mb-convert-variables.html) — Перетворює символи на змінну з одного кодування на інше
-   [мбdecodemimeheader](function.mb-decode-mimeheader.html) — Декодує рядок у MIME-заголовку
-   [мбdecodenumericentity](function.mb-decode-numericentity.html) — Декодує посилання на числовий рядок HTML на символ
-   [мбdetectencoding](function.mb-detect-encoding.html) — Визначення кодування символів
-   [мбdetectorder](function.mb-detect-order.html) — Встановлення/отримання списку кодувань для механізмів визначення кодування
-   [мбencodemimeheader](function.mb-encode-mimeheader.html) — Кодує рядок для MIME-заголовка
-   [мбencodenumericentity](function.mb-encode-numericentity.html) — Кодує символ у числове HTML-посилання
-   [мбencodingaliases](function.mb-encoding-aliases.html) — Отримує псевдоніми відомого типу кодування
-   [мбeregmatch](function.mb-ereg-match.html) — Збіг з регулярним виразом для багатобайтового рядка
-   [мбeregreplacecallback](function.mb-ereg-replace-callback.html) — Виконує пошук та заміну за регулярним виразом за допомогою багатобайтових кодувань використовуючи callback-функцію
-   [мбeregreplace](function.mb-ereg-replace.html) — Здійснює заміну за регулярним виразом за допомогою багатобайтових кодувань.
-   [мбeregsearchgetpos](function.mb-ereg-search-getpos.html) — Повертає початкову позицію наступного збігу з регулярним виразом
-   [мбeregsearchgetregs](function.mb-ereg-search-getregs.html) — Виводить результат останнього порівняння з регулярним виразом
-   [мбeregsearchinit](function.mb-ereg-search-init.html) — Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного вираження
-   [мбeregsearchpos](function.mb-ereg-search-pos.html) — Повертає позицію і довжину ділянки багатобайтового рядка, що збіглася з регулярним виразом.
-   [мбeregsearchregs](function.mb-ereg-search-regs.html) — Повертає частину рядка, що збіглася з регулярним виразом.
-   [мбeregsearchsetpos](function.mb-ereg-search-setpos.html) — Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу
-   [мбeregsearch](function.mb-ereg-search.html) — Пошук відповідності регулярному виразу для рядків у багатобайтових кодуваннях
-   [мбereg](function.mb-ereg.html) — Збіг з регулярним виразом із підтримкою багатобайтових кодувань
-   [мбeregireplace](function.mb-eregi-replace.html) — Здійснює заміну за регулярним виразом за допомогою багатобайтових символів без урахування регістру
-   [мбeregi](function.mb-eregi.html) — Пошук відповідності регулярному виразу за допомогою багатобайтових символів без урахування регістру
-   [мбgetinfo](function.mb-get-info.html) — Отримує внутрішні налаштування mbstring
-   [мбhttpinput](function.mb-http-input.html) — Визначення кодування символів вхідних даних HTTP-запиту
-   [мбhttpoutput](function.mb-http-output.html) — Встановлення/отримання кодування символів виводу HTTP
-   [мбinternalencoding](function.mb-internal-encoding.html) — Встановлення/отримання внутрішнього кодування скрипту
-   [мбlanguage](function.mb-language.html) — Встановлює/отримує поточну мову
-   [мбlistencodings](function.mb-list-encodings.html) — Повертає масив усіх кодувань, що підтримуються.
-   [мбord](function.mb-ord.html) — Отримує кодову точку символу Unicode
-   [мбoutputhandler](function.mb-output-handler.html) - Callback-функція, що перетворює кодування символів у вихідному буфері
-   [мбparsestr](function.mb-parse-str.html) — Розбір даних запитів GET/POST/COOKIE та встановлення значень глобальних змінних
-   [мбpreferredmimename](function.mb-preferred-mime-name.html) — Отримання набору символів MIME
-   [мбregexencoding](function.mb-regex-encoding.html) — Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбregexsetoptions](function.mb-regex-set-options.html) — Встановлення/отримання стандартних значень для налаштування функцій mbregex
-   [мбscrub](function.mb-scrub.html) - Опис
-   [мбsendmail](function.mb-send-mail.html) — Надсилання закодованого повідомлення
-   [мбsplit](function.mb-split.html) — Поділ рядків у багатобайтних кодуваннях, використовуючи регулярний вираз
-   [мбstrsplit](function.mb-str-split.html) — Якщо заданий багатобайтовий рядок повертає масив символів
-   [мбstrcut](function.mb-strcut.html) — Отримання частини рядка
-   [мбstrimwidth](function.mb-strimwidth.html) — Отримання рядка, обрізаного до заданого розміру
-   [мбstripos](function.mb-stripos.html) — Реєстронезалежний пошук позиції першого входження одного рядка в інший
-   [мбstristr](function.mb-stristr.html) — Знаходить перше входження підрядки у рядку без урахування регістру
-   [мбstrlen](function.mb-strlen.html) — Отримує довжину рядка
-   [мбstrpos](function.mb-strpos.html) — Пошук позиції першого входження одного рядка до іншого
-   [мбstrrchr](function.mb-strrchr.html) — Пошук останнього входження одного рядка до іншого
-   [мбstrrichr](function.mb-strrichr.html) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [мбstrripos](function.mb-strripos.html) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [мбstrrpos](function.mb-strrpos.html) — Пошук позиції останнього входження одного рядка до іншого
-   [мбstrstr](function.mb-strstr.html) — Знаходить перше входження підрядка у рядку
-   [мбstrtolower](function.mb-strtolower.html) — Приведення рядка до нижнього регістру
-   [мбstrtoupper](function.mb-strtoupper.html) — Приведення рядка до верхнього регістру
-   [мбstrwidth](function.mb-strwidth.html) — Повертає ширину рядка
-   [мбsubstitutecharacter](function.mb-substitute-character.html) — Встановити/отримати символ заміни
-   [мбsubstrcount](function.mb-substr-count.html) — Повертає кількість входжень підрядка
-   [мбsubstr](function.mb-substr.html) — Повертає частину рядка

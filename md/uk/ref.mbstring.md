---
navigation:
  - mbstring.php4.req.md: « Вимоги до кодування символів у PHP
  - function.mb-check-encoding.md: мбcheckencoding »
  - index.md: PHP Manual
  - book.mbstring.md: Багатобайтові рядки
title: Функції для роботи з багатобайтовими рядками
---
# Функції для роботи з багатобайтовими рядками

# Посилання

Схеми багатобайтного кодування символів та його реалізації досить складні, та його опис перебуває поза цієї документации. Більш вичерпну інформацію про кодування та їх пристрій можна отримати з наведених нижче джерел.

-   Матеріали по Юнікоду
    
    [» http://www.unicode.org/](http://www.unicode.org/)
    
-   Інформація про символи японського/корейського/китайського кодувань
    
    [» https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf](https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf)
    

## Зміст

-   [мбcheckencoding](function.mb-check-encoding.md) — Перевіряє, що кодування рядків вибрано правильно
-   [мбchr](function.mb-chr.md) — Повертає символ за значенням кодової точки Unicode
-   [мбconvertcase](function.mb-convert-case.md) — Здійснює зміну регістру символів у рядку
-   [мбconvertencoding](function.mb-convert-encoding.md) — Перетворює рядок з одного кодування символів на інший
-   [мбconvertkana](function.mb-convert-kana.md) - Перетворення кодувань "kana" з одного в інше ("zen-kaku", "han-kaku" та інші)
-   [мбconvertvariables](function.mb-convert-variables.md) — Перетворює символи на змінну з одного кодування на інше
-   [мбdecodemimeheader](function.mb-decode-mimeheader.md) — Декодує рядок у MIME-заголовку
-   [мбdecodenumericentity](function.mb-decode-numericentity.md) — Декодує посилання на числовий рядок HTML на символ
-   [мбdetectencoding](function.mb-detect-encoding.md) — Визначення кодування символів
-   [мбdetectorder](function.mb-detect-order.md) — Встановлення/отримання списку кодувань для механізмів визначення кодування
-   [мбencodemimeheader](function.mb-encode-mimeheader.md) — Кодує рядок для MIME-заголовка
-   [мбencodenumericentity](function.mb-encode-numericentity.md) — Кодує символ у числове HTML-посилання
-   [мбencodingaliases](function.mb-encoding-aliases.md) — Отримує псевдоніми відомого типу кодування
-   [мбeregmatch](function.mb-ereg-match.md) — Збіг з регулярним виразом для багатобайтового рядка
-   [мбeregreplacecallback](function.mb-ereg-replace-callback.md) — Виконує пошук та заміну за регулярним виразом за допомогою багатобайтових кодувань використовуючи callback-функцію
-   [мбeregreplace](function.mb-ereg-replace.md) — Здійснює заміну за регулярним виразом за допомогою багатобайтових кодувань.
-   [мбeregsearchgetpos](function.mb-ereg-search-getpos.md) — Повертає початкову позицію наступного збігу з регулярним виразом
-   [мбeregsearchgetregs](function.mb-ereg-search-getregs.md) — Виводить результат останнього порівняння з регулярним виразом
-   [мбeregsearchinit](function.mb-ereg-search-init.md) — Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного вираження
-   [мбeregsearchpos](function.mb-ereg-search-pos.md) — Повертає позицію і довжину ділянки багатобайтового рядка, що збіглася з регулярним виразом.
-   [мбeregsearchregs](function.mb-ereg-search-regs.md) — Повертає частину рядка, що збіглася з регулярним виразом.
-   [мбeregsearchsetpos](function.mb-ereg-search-setpos.md) — Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу
-   [мбeregsearch](function.mb-ereg-search.md) — Пошук відповідності регулярному виразу для рядків у багатобайтових кодуваннях
-   [мбereg](function.mb-ereg.md) — Збіг з регулярним виразом із підтримкою багатобайтових кодувань
-   [мбeregireplace](function.mb-eregi-replace.md) — Здійснює заміну за регулярним виразом за допомогою багатобайтових символів без урахування регістру
-   [мбeregi](function.mb-eregi.md) — Пошук відповідності регулярному виразу за допомогою багатобайтових символів без урахування регістру
-   [мбgetinfo](function.mb-get-info.md) — Отримує внутрішні налаштування mbstring
-   [мбhttpinput](function.mb-http-input.md) — Визначення кодування символів вхідних даних HTTP-запиту
-   [мбhttpoutput](function.mb-http-output.md) — Встановлення/отримання кодування символів виводу HTTP
-   [мбinternalencoding](function.mb-internal-encoding.md) — Встановлення/отримання внутрішнього кодування скрипту
-   [мбlanguage](function.mb-language.md) — Встановлює/отримує поточну мову
-   [мбlistencodings](function.mb-list-encodings.md) — Повертає масив усіх кодувань, що підтримуються.
-   [мбord](function.mb-ord.md) — Отримує кодову точку символу Unicode
-   [мбoutputhandler](function.mb-output-handler.md) - Callback-функція, що перетворює кодування символів у вихідному буфері
-   [мбparsestr](function.mb-parse-str.md) — Розбір даних запитів GET/POST/COOKIE та встановлення значень глобальних змінних
-   [мбpreferredmimename](function.mb-preferred-mime-name.md) — Отримання набору символів MIME
-   [мбregexencoding](function.mb-regex-encoding.md) — Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбregexsetoptions](function.mb-regex-set-options.md) — Встановлення/отримання стандартних значень для налаштування функцій mbregex
-   [мбscrub](function.mb-scrub.md) - Опис
-   [мбsendmail](function.mb-send-mail.md) — Надсилання закодованого повідомлення
-   [мбsplit](function.mb-split.md) — Поділ рядків у багатобайтних кодуваннях, використовуючи регулярний вираз
-   [мбstrsplit](function.mb-str-split.md) — Якщо заданий багатобайтовий рядок повертає масив символів
-   [мбstrcut](function.mb-strcut.md) — Отримання частини рядка
-   [мбstrimwidth](function.mb-strimwidth.md) — Отримання рядка, обрізаного до заданого розміру
-   [мбstripos](function.mb-stripos.md) — Реєстронезалежний пошук позиції першого входження одного рядка в інший
-   [мбstristr](function.mb-stristr.md) — Знаходить перше входження підрядки у рядку без урахування регістру
-   [мбstrlen](function.mb-strlen.md) — Отримує довжину рядка
-   [мбstrpos](function.mb-strpos.md) — Пошук позиції першого входження одного рядка до іншого
-   [мбstrrchr](function.mb-strrchr.md) — Пошук останнього входження одного рядка до іншого
-   [мбstrrichr](function.mb-strrichr.md) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [мбstrripos](function.mb-strripos.md) — Пошук останнього входження одного рядка в інший, нечутливий до регістру
-   [мбstrrpos](function.mb-strrpos.md) — Пошук позиції останнього входження одного рядка до іншого
-   [мбstrstr](function.mb-strstr.md) — Знаходить перше входження підрядка у рядку
-   [мбstrtolower](function.mb-strtolower.md) — Приведення рядка до нижнього регістру
-   [мбstrtoupper](function.mb-strtoupper.md) — Приведення рядка до верхнього регістру
-   [мбstrwidth](function.mb-strwidth.md) — Повертає ширину рядка
-   [мбsubstitutecharacter](function.mb-substitute-character.md) — Встановити/отримати символ заміни
-   [мбsubstrcount](function.mb-substr-count.md) — Повертає кількість входжень підрядка
-   [мбsubstr](function.mb-substr.md) — Повертає частину рядка

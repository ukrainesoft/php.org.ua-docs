---
navigation:
  - function.wordwrap.md: « wordwrap
  - refs.basic.vartype.md: 'Модулі, що відносяться до змінних та типів »'
  - index.md: PHP Manual
  - book.strings.md: Рядки
title: список змін
---
# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function | Description |
| --- | --- | --- |
|  | [utf8decode](function.utf8-decode.md) | Функцію оголошено застарілою. |
|  | [utf8encode](function.utf8-encode.md) | Ця функція має бути неперевіреною. |
|  | [gethtmltranslationtable](function.get-html-translation-table.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlentitydecode](function.html-entity-decode.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlentities](function.htmlentities.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialchars](function.htmlspecialchars.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialcharsdecode](function.htmlspecialchars-decode.md) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [convertuuencode](function.convert-uuencode.md) | До цієї версії при спробі перетворити порожній рядок поверталося false без особливих причин. |
|  | [countchars](function.count-chars.md) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [crypt](function.crypt.md) | salt більше не є необов'язковим. |
|  | [explode](function.explode.md) | explode тепер викидає TypeError, якщо параметр separator є порожнім рядком (""). Раніше замість вилучення explode повертала false. |
|  | [htmlentitydecode](function.html-entity-decode.md) | encoding тепер допускає значення null. |
|  | [htmlentities](function.htmlentities.md) | encoding тепер допускає значення null. |
|  | [implode](function.implode.md) | Передача separator після array більше не підтримується. |
|  | [levenshtein](function.levenshtein.md) | До цієї версії levenshtein потрібно було викликати з двома чи п'ятьма аргументами. |
|  | [metaphone](function.metaphone.md) | Функція повертала false у разі виникнення помилки. |
|  | [numberformat](function.number-format.md) | До цієї версії функція numberformat приймала один, два чи чотири параметри (але не три). |
|  | [parsestr](function.parse-str.md) | result більше не є необов'язковим. |
|  | [soundex](function.soundex.md) | До цієї версії при виклику функції з порожнім рядком поверталося false без особливих причин. |
|  | [sprintf](function.sprintf.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [strsplit](function.str-split.md) | Тепер якщо параметр length менший за 1, буде викинута помилка ValueError; раніше, натомість видавалася помилка рівня EWARNING, а функція повертала false. |
|  | [strwordcount](function.str-word-count.md) | characters тепер допускає значення null. |
|  | [strcspn](function.strcspn.md) | length тепер припускає значення null. |
|  | [striptags](function.strip-tags.md) | allowedtags тепер допускає значення null. |
|  | [stripos](function.stripos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [stristr](function.stristr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strpos](function.strpos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrchr](function.strrchr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strripos](function.strripos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrpos](function.strrpos.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strspn](function.strspn.md) | length тепер припускає значення null. |
|  | [strstr](function.strstr.md) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [substr](function.substr.md) | Параметр length тепер припускає значення null. Якщо значення length явно задано як null, функція повертає підрядок, що закінчується в кінці рядка; раніше повертався порожній рядок. |
|  | [substr](function.substr.md) | Функція повертає порожній рядок, де раніше повертала false. |
|  | [substrcompare](function.substr-compare.md) | length тепер припускає значення null. |
|  | [substrcount](function.substr-count.md) | length тепер припускає значення null. |
|  | [substrreplace](function.substr-replace.md) | length тепер припускає значення null. |
|  | [vsprintf](function.vsprintf.md) | Функція більше не повертає false у разі виникнення помилки. |
|  | [chr](function.chr.md) | Функція більше не приймає непідтримувані значення codepoint і перетворює їх на 0. |
|  | [implode](function.implode.md) | Передача separator після array (тобто використання недокументованого порядку параметрів) застаріла. |
|  | [moneyformat](function.money-format.md) | Функція застаріла. Замість неї використовуйте NumberFormatter::formatCurrency. |
|  | [strgetcsv](function.str-getcsv.md) | Тепер порожній параметр escape інтерпретуватиметься як вимога вимкнення пропрієтарного механізму екранування. Раніше порожній рядок позначав використання символу екранування за промовчанням. |
|  | [striptags](function.strip-tags.md) | allowedtags альтернативно приймає масив (array). |
|  | [stripos](function.stripos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [stristr](function.stristr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strpos](function.strpos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrchr](function.strrchr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strripos](function.strripos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrpos](function.strrpos.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strstr](function.strstr.md) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [substrcompare](function.substr-compare.md) | offset тепер може бути рівним haystack. |
|  | [numberformat](function.number-format.md) | numberformat була змінена, щоб не повертати -0, раніше -0 могло бути повернено у випадках коли num був -0.01. |
|  | [parsestr](function.parse-str.md) | Використання parsestr без другого параметра буде викликати помилку рівня EDEPRECATED. |
|  | [utf8decode](function.utf8-decode.md) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [utf8encode](function.utf8-encode.md) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [strshuffle](function.str-shuffle.md) | Внутрішній алгоритм отримання випадкових чисел змінено з функції rand бібліотеки libc на генератор з урахуванням Вихря Мерсена. |
|  | [stripos](function.stripos.md) | Додано підтримку негативних значень offset. |
|  | [strpos](function.strpos.md) | Додано підтримку негативних значень offset. |
|  | [substrcount](function.substr-count.md) | Додано підтримку негативних значень offset і length. length тепер також може бути 0. |

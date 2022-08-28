список змін

-   [« wordwrap](function.wordwrap.html)
    
-   [Модули, относящиеся к переменным и типам »](refs.basic.vartype.html)
    
-   [PHP Manual](index.html)
    
-   [Строки](book.strings.html)
    
-   список змін
    

# список змін

Наступні зміни були здійснені з класами/функціями/методами даного модуля.

| Version | Function | Description |
| --- | --- | --- |
|  | [utf8\_decode](function.utf8-decode.html) | Функцію оголошено застарілою. |
|  | [utf8\_encode](function.utf8-encode.html) | Ця функція має бути неперевіреною. |
|  | [get\_html\_translation\_table](function.get-html-translation-table.html) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [html\_entity\_decode](function.html-entity-decode.html) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlentities](function.htmlentities.html) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialchars](function.htmlspecialchars.html) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [htmlspecialchars\_decode](function.htmlspecialchars-decode.html) | Значення за замовчуванням параметра flags змінено з ENTCOMPAT на ENTQUOTES |
|  | [convert\_uuencode](function.convert-uuencode.html) | До цієї версії при спробі перетворити порожній рядок поверталося false без особливих причин. |
|  | [count\_chars](function.count-chars.html) | До цієї версії функція повертала false у разі виникнення помилки. |
|  | [crypt](function.crypt.html) | salt більше не є необов'язковим. |
|  | [explode](function.explode.html) | explode тепер викидає TypeError, якщо параметр separator є порожнім рядком (""). Раніше замість вилучення explode повертала false. |
|  | [html\_entity\_decode](function.html-entity-decode.html) | encoding тепер допускає значення null. |
|  | [htmlentities](function.htmlentities.html) | encoding тепер допускає значення null. |
|  | [implode](function.implode.html) | Передача separator після array більше не підтримується. |
|  | [levenshtein](function.levenshtein.html) | До цієї версії levenshtein потрібно було викликати з двома чи п'ятьма аргументами. |
|  | [metaphone](function.metaphone.html) | Функція повертала false у разі виникнення помилки. |
|  | [number\_format](function.number-format.html) | До цієї версії функція numberformat приймала один, два чи чотири параметри (але не три). |
|  | [parse\_str](function.parse-str.html) | result більше не є необов'язковим. |
|  | [soundex](function.soundex.html) | До цієї версії при виклику функції з порожнім рядком поверталося false без особливих причин. |
|  | [sprintf](function.sprintf.html) | Функція більше не повертає false у разі виникнення помилки. |
|  | [str\_split](function.str-split.html) | Тепер якщо параметр length менший за 1, буде викинута помилка ValueError; раніше, натомість видавалася помилка рівня EWARNING, а функція повертала false. |
|  | [str\_word\_count](function.str-word-count.html) | characters тепер допускає значення null. |
|  | [strcspn](function.strcspn.html) | length тепер припускає значення null. |
|  | [strip\_tags](function.strip-tags.html) | allowedtags тепер допускає значення null. |
|  | [stripos](function.stripos.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [stristr](function.stristr.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strpos](function.strpos.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrchr](function.strrchr.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strripos](function.strripos.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strrpos](function.strrpos.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [strspn](function.strspn.html) | length тепер припускає значення null. |
|  | [strstr](function.strstr.html) | Передача цілого числа (int) у needle більше не підтримується. |
|  | [substr](function.substr.html) | Параметр length тепер припускає значення null. Якщо значення length явно задано як null, функція повертає підрядок, що закінчується в кінці рядка; раніше повертався порожній рядок. |
|  | [substr](function.substr.html) | Функція повертає порожній рядок, де раніше повертала false. |
|  | [substr\_compare](function.substr-compare.html) | length тепер припускає значення null. |
|  | [substr\_count](function.substr-count.html) | length тепер припускає значення null. |
|  | [substr\_replace](function.substr-replace.html) | length тепер припускає значення null. |
|  | [vsprintf](function.vsprintf.html) | Функція більше не повертає false у разі виникнення помилки. |
|  | [chr](function.chr.html) | Функція більше не приймає непідтримувані значення codepoint і перетворює їх на 0. |
|  | [implode](function.implode.html) | Передача separator після array (тобто використання недокументованого порядку параметрів) застаріла. |
|  | [money\_format](function.money-format.html) | Функція застаріла. Замість неї використовуйте NumberFormatter::formatCurrency. |
|  | [str\_getcsv](function.str-getcsv.html) | Тепер порожній параметр escape інтерпретуватиметься як вимога вимкнення пропрієтарного механізму екранування. Раніше порожній рядок позначав використання символу екранування за промовчанням. |
|  | [strip\_tags](function.strip-tags.html) | allowedtags альтернативно приймає масив (array). |
|  | [stripos](function.stripos.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [stristr](function.stristr.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strpos](function.strpos.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrchr](function.strrchr.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strripos](function.strripos.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strrpos](function.strrpos.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [strstr](function.strstr.html) | Передача цілого числа (int) у needle оголошена застарілою. |
|  | [substr\_compare](function.substr-compare.html) | offset тепер може бути рівним haystack. |
|  | [number\_format](function.number-format.html) | numberformat була змінена, щоб не повертати -0, раніше -0 могло бути повернено у випадках коли num був -0.01. |
|  | [parse\_str](function.parse-str.html) | Використання parsestr без другого параметра буде викликати помилку рівня EDEPRECATED. |
|  | [utf8\_decode](function.utf8-decode.html) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [utf8\_encode](function.utf8-encode.html) | Функцію було перенесено з модуля XML в ядро ​​PHP. У попередніх версіях вона була доступна лише за встановленого модуля XML. |
|  | [str\_shuffle](function.str-shuffle.html) | Внутрішній алгоритм отримання випадкових чисел змінено з функції rand бібліотеки libc на генератор з урахуванням Вихря Мерсена. |
|  | [stripos](function.stripos.html) | Додано підтримку негативних значень offset. |
|  | [strpos](function.strpos.html) | Додано підтримку негативних значень offset. |
|  | [substr\_count](function.substr-count.html) | Додано підтримку негативних значень offset і length. length тепер також може бути 0. |
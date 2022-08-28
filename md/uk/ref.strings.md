Функції для роботи з рядками

-   [« Предопределённые константы](string.constants.html)
    
-   [addcslashes »](function.addcslashes.html)
    
-   [PHP Manual](index.html)
    
-   [Строки](book.strings.html)
    
-   Функції для роботи з рядками
    

# Функції для роботи з рядками

# Дивіться також

Для отримання інформації про більш складну обробку рядків зверніться до [функциями Perl-совместимых регулярных выражений](ref.pcre.html). Для роботи з багатобайтовими кодуваннями подивіться на [функции по работе с многобайтовыми кодировками](ref.mbstring.html)

## Зміст

-   [addcslashes](function.addcslashes.html) — Екранує рядок слішами у стилі мови C
-   [addslashes](function.addslashes.html) — Екранує рядок за допомогою слішів
-   [bin2hex](function.bin2hex.html) — Перетворює бінарні дані на шістнадцяткову виставу
-   [chop](function.chop.html) - Псевдонім rtrim
-   [chr](function.chr.html) — Генерує односимвольний рядок за заданим числом
-   [chunk\_split](function.chunk-split.html) - Розбиває рядок на фрагменти
-   [convert\_cyr\_string](function.convert-cyr-string.html) — Перетворює рядок з одного кириличного кодування на інше
-   [convert\_uudecode](function.convert-uudecode.html) — Декодує рядок із формату uuencode у звичайний вигляд
-   [convert\_uuencode](function.convert-uuencode.html) — Кодує рядок у форматі uuencode
-   [count\_chars](function.count-chars.html) — Повертає інформацію про символи, що входять до рядка
-   [crc32](function.crc32.html) — Обчислює поліном CRC32 для рядка
-   [crypt](function.crypt.html) — Необоротне хешування рядка
-   [echo](function.echo.html) — Виводить один або більше рядків
-   [explode](function.explode.html) — Розбиває рядок за допомогою роздільника
-   [fprintf](function.fprintf.html) — Записує відформатований рядок у потік
-   [get\_html\_translation\_table](function.get-html-translation-table.html) — Повертає таблицю перетворень, використовувану функціями htmlspecialchars і htmlentities
-   [hebrev](function.hebrev.html) — Перетворює текст на івриті з логічного кодування на візуальне
-   [hebrevc](function.hebrevc.html) — Перетворює текст на івриті з логічного кодування на візуальне з перетворенням перекладу рядка
-   [hex2bin](function.hex2bin.html) — Перетворює шістнадцяткові дані на двійкові
-   [html\_entity\_decode](function.html-entity-decode.html) — Перетворює HTML-сутності у відповідні символи
-   [htmlentities](function.htmlentities.html) — Перетворює всі можливі символи у відповідні HTML-сутності
-   [htmlspecialchars\_decode](function.htmlspecialchars-decode.html) — Перетворює спеціальні HTML-сутності назад на відповідні символи
-   [htmlspecialchars](function.htmlspecialchars.html) — Перетворює спеціальні символи на HTML-сутності
-   [implode](function.implode.html) — Об'єднує елементи масиву в рядок
-   [join](function.join.html) - Псевдонім implode
-   [lcfirst](function.lcfirst.html) — Перетворює перший символ рядка на нижній регістр
-   [levenshtein](function.levenshtein.html) — Обчислює відстань Левенштейна між двома рядками
-   [localeconv](function.localeconv.html) — Повертає інформацію про форматування чисел
-   [ltrim](function.ltrim.html) — Видаляє прогалини (або інші символи) з початку рядка
-   [md5\_file](function.md5-file.html) — Повертає MD5-хеш файлу
-   [md5](function.md5.html) — Повертає MD5-хеш рядки
-   [metaphone](function.metaphone.html) — Повертає ключ metaphone для рядка
-   [money\_format](function.money-format.html) — Форматує число як грошову величину
-   [nl\_langinfo](function.nl-langinfo.html) — Повертає інформацію про мову та локалі
-   [nl2br](function.nl2br.html) — Вставляє HTML код розриву рядка перед кожним перекладом рядка
-   [number\_format](function.number-format.html) — Форматує число із поділом груп
-   [ord](function.ord.html) - Конвертує перший байт рядка в число від 0 до 255
-   [parse\_str](function.parse-str.html) — Розбирає рядок у змінні
-   [print](function.print.html) - Виводить рядок
-   [printf](function.printf.html) — Виводить відформатований рядок
-   [quoted\_printable\_decode](function.quoted-printable-decode.html) — Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок
-   [quoted\_printable\_encode](function.quoted-printable-encode.html) — Перетворює 8-бітовий рядок за допомогою методу quoted-printable
-   [quotemeta](function.quotemeta.html) — Екранує спеціальні символи
-   [rtrim](function.rtrim.html) — Видаляє прогалини (або інші символи) з кінця рядка
-   [setlocale](function.setlocale.html) - Встановлює налаштування локалі
-   [sha1\_file](function.sha1-file.html) - Повертає SHA1-хеш файлу
-   [sha1](function.sha1.html) - Повертає SHA1-хеш рядки
-   [similar\_text](function.similar-text.html) - Обчислює ступінь схожості двох рядків
-   [soundex](function.soundex.html) — Повертає ключ soundex для рядка
-   [sprintf](function.sprintf.html) — Повертає відформатований рядок
-   [sscanf](function.sscanf.html) — Розбирає рядок відповідно до заданого формату
-   [str\_contains](function.str-contains.html) — Визначає, чи містить рядок заданий підрядок
-   [str\_ends\_with](function.str-ends-with.html) — Перевіряє, чи рядок закінчується заданим підрядком
-   [str\_getcsv](function.str-getcsv.html) — Розбирає CSV-рядки в масив.
-   [str\_ireplace](function.str-ireplace.html) — Реєстронезалежний варіант функції strreplace
-   [str\_pad](function.str-pad.html) — Доповнює рядок іншим рядком до заданої довжини
-   [str\_repeat](function.str-repeat.html) — Повертає рядок, що повторюється.
-   [str\_replace](function.str-replace.html) — Замінює всі входження рядка пошуку на рядок заміни
-   [str\_rot13](function.str-rot13.html) — Виконує перетворення ROT13 над рядком
-   [str\_shuffle](function.str-shuffle.html) — Переставляє символи у рядку випадковим чином
-   [str\_split](function.str-split.html) — Перетворює рядок на масив
-   [str\_starts\_with](function.str-starts-with.html) — Перевіряє, чи починається рядок із заданого підрядку
-   [str\_word\_count](function.str-word-count.html) — Повертає інформацію про слова, що входять до рядка
-   [strcasecmp](function.strcasecmp.html) — Бінарно-безпечне порівняння рядків без урахування регістру
-   [strchr](function.strchr.html) - Псевдонім strstr
-   [strcmp](function.strcmp.html) - Бінарно-безпечне порівняння рядків
-   [strcoll](function.strcoll.html) — Порівняння рядків з урахуванням поточної локалі
-   [strcspn](function.strcspn.html) — Повертає довжину ділянки на початку рядка, що не відповідає масці
-   [strip\_tags](function.strip-tags.html) — Видаляє теги HTML та PHP з рядка
-   [stripcslashes](function.stripcslashes.html) — Видаляє екранування символів, зроблене функцією addcslashes
-   [stripos](function.stripos.html) — Повертає позицію першого входження підрядка без урахування регістру
-   [stripslashes](function.stripslashes.html) — Видаляє екранування символів
-   [stristr](function.stristr.html) — Реєстронезалежний варіант функції strstr
-   [strlen](function.strlen.html) — Повертає довжину рядка
-   [strnatcasecmp](function.strnatcasecmp.html) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
-   [strnatcmp](function.strnatcmp.html) - Порівняння рядків з використанням алгоритму "natural order"
-   [strncasecmp](function.strncasecmp.html) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strncmp](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [strpbrk](function.strpbrk.html) — Шукає у рядку будь-який символ із заданого набору
-   [strpos](function.strpos.html) — Повертає позицію першого входження підрядка
-   [strrchr](function.strrchr.html) — Знаходить останнє входження символу у рядку
-   [strrev](function.strrev.html) — Перевертає рядок задом наперед
-   [strripos](function.strripos.html) — Повертає позицію останнього входження підрядка без урахування регістру
-   [strrpos](function.strrpos.html) — Повертає позицію останнього входження підрядка у рядку
-   [strspn](function.strspn.html) — Повертає довжину ділянки на початку рядка, що повністю відповідає масці
-   [strstr](function.strstr.html) - Знаходить перше входження підрядка
-   [strtok](function.strtok.html) - Розбиває рядок на токени
-   [strtolower](function.strtolower.html) — Перетворює рядок на нижній регістр
-   [strtoupper](function.strtoupper.html) — Перетворює рядок у верхній регістр
-   [strtr](function.strtr.html) — Перетворює задані символи або замінює підрядки
-   [substr\_compare](function.substr-compare.html) - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [substr\_count](function.substr-count.html) — Повертає кількість входжень підрядка
-   [substr\_replace](function.substr-replace.html) — Замінює частину рядка
-   [substr](function.substr.html) - Повертає підрядок
-   [trim](function.trim.html) — Видаляє прогалини (або інші символи) з початку та кінця рядка
-   [ucfirst](function.ucfirst.html) — Перетворює перший символ рядка у верхній регістр
-   [ucwords](function.ucwords.html) — Перетворює на верхній регістр перший символ кожного слова в рядку
-   [utf8\_decode](function.utf8-decode.html) — Перетворює рядок з UTF-8 на ISO-8859-1, замінюючи неприпустимі або непредставні символи
-   [utf8\_encode](function.utf8-encode.html) — Перетворює рядок із ISO-8859-1 на UTF-8
-   [vfprintf](function.vfprintf.html) — Записує відформатований рядок у потік
-   [vprintf](function.vprintf.html) — Виводить відформатований рядок
-   [vsprintf](function.vsprintf.html) — Повертає відформатований рядок
-   [wordwrap](function.wordwrap.html) — Переносить рядок за вказаною кількістю символів
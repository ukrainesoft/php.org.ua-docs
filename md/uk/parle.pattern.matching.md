Зіставлення з шаблоном Parle

-   [« Обумовлені константи](parle.constants.html)
    
-   [Представления символов »](parle.regex.chars.html)
    
-   [PHP Manual](index.html)
    
-   [Parle](book.parle.html)
    
-   Зіставлення з шаблоном Parle
    

# Зіставлення з шаблоном Parle

## Зміст

-   [Представления символов](parle.regex.chars.html)
-   [Класи символів](parle.regex.charclass.html)
-   [Класи символів Unicode](parle.regex.unicodecharclass.html)
-   [Чередование и повторение](parle.regex.alternation.html)
-   [Якоря](parle.regex.anchors.html)
-   [Угруповання](parle.regex.grouping.html)

Parle підтримує зіставлення регулярних виразів аналогічно flex. Також підтримуються такі набори символів POSIX: `[:alnum:]` `[:alpha:]` `[:blank:]` `[:cntrl:]` `[:digit:]` `[:graph:]` `[:lower:]` `[:print:]` `[:punct:]` `[:space:]` `[:upper:]` і `[:xdigit:]`

Класи символів Unicode в даний час не включені за промовчанням, передайте --enable-parle-utf32, щоб зробити їх доступними. Конкретне кодування може відображатися за допомогою правильно побудованого регулярного виразу. Наприклад, щоб відповідати символу євро, закодованому в UTF-8, можна використовувати регулярний вираз `[\xe2][\x82][\xac]`. Шаблон для рядка кодування UTF-8 може бути `[ -\x7f]{+}[\x80-\xbf]{+}[\xc2-\xdf]{+}[\xe0-\xef]{+}[\xf0-\xff]+`
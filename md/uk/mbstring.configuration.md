Налаштування під час виконання

-   [« Установка](mbstring.installation.html)
    
-   [Типы ресурсов »](mbstring.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mbstring.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції конфігурації mbstring**

| Имя                                                                                                           | По умолчанию | Место изменения         | Список изменений                                        |
|---------------------------------------------------------------------------------------------------------------|--------------|-------------------------|---------------------------------------------------------|
| [mbstring.language](mbstring.configuration.html#ini.mbstring.language)                                        | "neutral"    | PHPINIALL               |                                                         |
| [mbstring.detect\_order](mbstring.configuration.html#ini.mbstring.detect-order)                               | NULL         | PHPINIALL               |                                                         |
| [mbstring.http\_input](mbstring.configuration.html#ini.mbstring.http-input)                                   | "pass"       | PHPINIALL               | Застаріла                                               |
| [mbstring.http\_output](mbstring.configuration.html#ini.mbstring.http-output)                                 | "pass"       | PHPINIALL               | Застаріла                                               |
| [mbstring.internal\_encoding](mbstring.configuration.html#ini.mbstring.internal-encoding)                     | NULL         | PHPINIALL               | Застаріла                                               |
| [mbstring.substitute\_character](mbstring.configuration.html#ini.mbstring.substitute-character)               | NULL         | PHPINIALL               |                                                         |
| [mbstring.func\_overload](mbstring.configuration.html#ini.mbstring.func-overload)                             | "0"          | PHPINISYSTEM            | Оголошено застарілим у PHP 7.2.0; видалено з PHP 8.0.0. |
| [mbstring.encoding\_translation](mbstring.configuration.html#ini.mbstring.encoding-translation)               | "0"          | PHPINIPERDIR            |                                                         |
| [mbstring.http\_output\_conv\_mimetypes](mbstring.configuration.html#ini.mbstring.http-output-conv-mimetypes) | "^(text/     | application/xhtml+xml)" | PHPINIALL                                               |
| [mbstring.strict\_detection](mbstring.configuration.html#ini.mbstring.strict-detection)                       | "0"          | PHPINIALL               |                                                         |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`mbstring.language` string

За замовчуванням у mbstring використовуються налаштування національної мови. Зверніть увагу, що ця опція автоматично визначає `mbstring.internal_encoding`, і `mbstring.internal_encoding` повинен бути поміщений після `mbstring.language` у php.ini

`mbstring.encoding_translation` bool

Включає прозорий фільтр кодування для вхідних запитів HTTP, який здійснює виявлення та перетворення вхідного кодування у внутрішнє кодування.

`mbstring.internal_encoding` string

**Увага**

Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому.

Визначає внутрішнє кодування символів за промовчанням.

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.html#ini.default-charset)

`mbstring.http_input` string

**Увага**

Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому.

Визначає кодування символів за промовчанням для введення HTTP.

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.html#ini.default-charset)

`mbstring.http_output` string

**Увага**

Ця можливість застаріла та *буде* обов'язково *видалено* в майбутньому.

Визначає кодування символів за промовчанням для HTTP-виводу (конвертація з внутрішнього кодування в кодування HTTP виводу відбудеться перед виведенням).

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.html#ini.default-charset)

`mbstring.detect_order` string

Визначає порядок визначення кодування символів за промовчанням. Дивіться також [mb\_detect\_order()](function.mb-detect-order.html)

`mbstring.substitute_character` string

Визначає символ для заміни неприпустимих символів кодування. Список підтримуваних значень дивіться в описі функції [mb\_substitute\_character()](function.mb-substitute-character.html)

`mbstring.func_overload` string

**Увага**

Ця функціональність оголошена *застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Перевантажує безліч однобайтових функцій аналогами з mbstring. Дивіться розділ [Перегрузка функций](mbstring.overload.html) для отримання додаткової інформації.

Ця опція може бути змінена лише у файлі php.ini.

`mbstring.http_output_conv_mimetypes` string

`mbstring.strict_detection` bool

Включає чітке визначення кодування. Дивіться опис та приклади в [mb\_detect\_encoding()](function.mb-detect-encoding.html)

Згідно [» спецификации HTML 4.01](http://www.w3.org/TR/REC-html40/interact/forms.html#adef-accept-charset), веб-браузерам дозволено перекодувати дані з форми, які вони набувають у кодуванні символів, відмінної від використовуваної на сторінці. Дивіться функцію [mb\_http\_input()](function.mb-http-input.html) для того, щоб визначити кодування символів, що використовується браузерами.

Хоча популярні браузери здатні досить точно визначити кодування символів даного HTML-документа, краще встановити параметр `charset` у HTTP-заголовку `Content-Type` відповідним значенням за допомогою [header()](function.header.html) або вказати потрібне значення у параметрі [default\_charset](ini.core.html#ini.sect.data-handling) в ini-налаштуваннях.

**Приклад #1 Приклади налаштувань php.ini**

```
; Установить язык по умолчанию
mbstring.language        = Neutral; Установить Neutral(UTF-8) языком по умолчанию (по умолчанию)
mbstring.language        = English; Установить английский языком по умолчанию
mbstring.language        = Japanese; Установить японский языком по умолчанию

;; Установить внутреннюю кодировку по умолчанию
;; Примечание: Убедитесь, что используете кодировку символов, которая работает с PHP
mbstring.internal_encoding    = UTF-8  ; Установить внутреннюю кодировку в UTF-8

;; Включено преобразование кодировки HTTP-ввода.
mbstring.encoding_translation = On

;; Установить кодировку символов по умолчанию для HTTP-ввода
;; Примечание: Скрипт не может изменить установку http_input.
mbstring.http_input           = pass    ; Нет преобразования.
mbstring.http_input           = auto    ; Установить HTTP-ввод в auto
                                ; "auto" расширяется в соответствии с mbstring.language
mbstring.http_input           = SJIS    ; Установить HTTP-ввод в SJIS
mbstring.http_input           = UTF-8,SJIS,EUC-JP ; Указать порядок

;; Установить кодировку символов по умолчанию для HTTP-вывода
mbstring.http_output          = pass    ; Нет преобразования.
mbstring.http_output          = UTF-8   ; Установить кодировку HTTP-вывода в UTF-8

;; Установить порядок определения кодировки символов по умолчанию
mbstring.detect_order         = auto    ; Установить порядок определения в auto
mbstring.detect_order         = ASCII,JIS,UTF-8,SJIS,EUC-JP ; Указать порядок

;; Установить символ замены по умолчанию
mbstring.substitute_character = 12307   ; Указать значение Unicode
mbstring.substitute_character = none    ; Не печатать символ
mbstring.substitute_character = long    ; Примеры кодовых значений символов: U+3000,JIS+7E7E
```

**Приклад #2 Налаштування php.ini для користувачів `EUC-JP`**

```
;; Отключить буферизацию вывода
output_buffering      = Off

;; Установить кодировку в http-заголовке
default_charset       = EUC-JP

;; Установить японский языком по умолчанию
mbstring.language = Japanese

;; Включено преобразование кодировки HTTP-ввода.
mbstring.encoding_translation = On

;; Установить перекодировку HTTP-ввода в auto
mbstring.http_input   = auto

;; Конвертировать HTTP-вывод в EUC-JP
mbstring.http_output  = EUC-JP

;; Установить внутреннюю кодировку в EUC-JP
mbstring.internal_encoding = EUC-JP

;; Не печатать недопустимые символы
mbstring.substitute_character = none
```

**Приклад #3 Налаштування php.ini для користувачів `SJIS`**

```
;; Включить буферизацию вывода
output_buffering     = On

;; Установить mb_output_handler для включения перекодировки вывода
output_handler       = mb_output_handler

;; Установить кодировку в http-заголовке
default_charset      = Shift_JIS

;; Установить японский языком по умолчанию
mbstring.language = Japanese

;; Установить перекодировку HTTP-ввода в auto
mbstring.http_input  = auto

;; Конвертировать в SJIS
mbstring.http_output = SJIS

;; Установить внутреннюю кодировку в EUC-JP
mbstring.internal_encoding = EUC-JP

;; Не печатать недопустимые символы
mbstring.substitute_character = none
```
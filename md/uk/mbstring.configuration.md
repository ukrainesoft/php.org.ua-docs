---
navigation:
  - mbstring.installation.md: « Встановлення
  - mbstring.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mbstring.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції конфігурації mbstring**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mbstring.language](mbstring.configuration.md#ini.mbstring.language) | "neutral" | **`INI_ALL`** |  |
| [mbstring.detect\_order](mbstring.configuration.md#ini.mbstring.detect-order) | NULL | **`INI_ALL`** |  |
| [mbstring.http\_input](mbstring.configuration.md#ini.mbstring.http-input) | "pass" | **`INI_ALL`** | Застаріла |
| [mbstring.http\_output](mbstring.configuration.md#ini.mbstring.http-output) | "pass" | **`INI_ALL`** | Застаріла |
| [mbstring.internal\_encoding](mbstring.configuration.md#ini.mbstring.internal-encoding) | NULL | **`INI_ALL`** | Застаріла |
| [mbstring.substitute\_character](mbstring.configuration.md#ini.mbstring.substitute-character) | NULL | **`INI_ALL`** |  |
| [mbstring.func\_overload](mbstring.configuration.md#ini.mbstring.func-overload) | "0" | **`INI_SYSTEM`** | Оголошено застарілим у PHP 7.2.0; видалено з PHP 8.0.0. |
| [mbstring.encoding\_translation](mbstring.configuration.md#ini.mbstring.encoding-translation) | "0" | **`INI_PERDIR`** |  |
| [mbstring.http\_output\_conv\_mimetypes](mbstring.configuration.md#ini.mbstring.http-output-conv-mimetypes) | "^(text/ | application/xhtml\\+xml)" | **`INI_ALL`** |
| [mbstring.strict\_detection](mbstring.configuration.md#ini.mbstring.strict-detection) | "0" | **`INI_ALL`** |  |
| [mbstring.regex\_retry\_limit](mbstring.configuration.md#ini.mbstring.regex-retry-limit) | "1000000" | **`INI_ALL`** | Доступно з PHP 7.4.0. |
| [mbstring.regex\_stack\_limit](mbstring.configuration.md#ini.mbstring.regex-stack-limit) | "100000" | **`INI_ALL`** | Доступно з PHP 7.3.5. |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`mbstring.language`string

За замовчуванням у mbstring використовуються налаштування національної мови. Зверніть увагу, що ця опція автоматично визначає `mbstring.internal_encoding`, и`mbstring.internal_encoding` повинен бути поміщений після `mbstring.language`в php.ini

`mbstring.encoding_translation`bool

Включає прозорий фільтр кодування для вхідних запитів HTTP, який виконує виявлення та перетворення вхідного кодування у внутрішнє кодування.

`mbstring.internal_encoding`string

**Увага**

Ця можливість застаріла та *буде* *видалено*в будущем.

Визначає внутрішнє кодування символів за промовчанням.

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.md#ini.default-charset)

`mbstring.http_input`string

**Увага**

Ця можливість застаріла та *буде* *видалено*в будущем.

Визначає кодування символів за промовчанням для введення HTTP.

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.md#ini.default-charset)

`mbstring.http_output`string

**Увага**

Ця можливість застаріла та *буде* *видалено*в будущем.

Визначає кодування символів за замовчуванням для виводу HTTP (конвертація з внутрішнього кодування в кодування виводу HTTP відбудеться перед виведенням).

Користувачі повинні залишити цю опцію порожньою та поставити замість неї [`default_charset`](ini.core.md#ini.default-charset)

`mbstring.detect_order`string

Определяет порядок определения кодировки символов по умолчанию. Смотрите также[mb\_detect\_order()](function.mb-detect-order.md)

`mbstring.substitute_character`string

Визначає символ для заміни неприпустимих символів кодування. Список підтримуваних значень дивіться в описі функції [mb\_substitute\_character()](function.mb-substitute-character.md)

`mbstring.func_overload`string

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

Перевантажує безліч однобайтових функцій аналогами з mbstring. Дивіться розділ [Перевантаження функцій](mbstring.overload.md) для отримання додаткової інформації.

Ця опція може бути змінена лише у файлі php.ini.

`mbstring.http_output_conv_mimetypes`string

`mbstring.strict_detection`bool

Включає чітке визначення кодування. Дивіться опис та приклади в [mb\_detect\_encoding()](function.mb-detect-encoding.md)

`mbstring.regex_retry_limit`int

Обмежує кількість зворотних ходів, які можуть бути виконані під час одного збігу mbregex.

Ця установка діє лише при зв'язуванні з oniguruma >= 6.8.0.

`mbstring.regex_stack_limit`int

Обмежує глибину стека регулярних виразів mbstring.

Согласно[» Специфікації HTML 4.01](http://www.w3.org/TR/REC-html40/interact/forms.md#adef-accept-charset), веб-браузерам дозволено перекодувати дані з форми, які вони набувають у кодуванні символів, відмінної від використовуваної на сторінці. Дивіться функцію [mb\_http\_input()](function.mb-http-input.md) для того, щоб визначити кодування символів, що використовується браузерами.

Хоча популярні браузери здатні досить точно визначити кодування символів даного HTML-документа, краще встановити параметр `charset` у HTTP-заголовку `Content-Type` відповідним значенням за допомогою [header()](function.header.md)или указать требуемое значение в параметре[default\_charset](ini.core.md#ini.sect.data-handling) в ini-налаштуваннях.

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
